---
layout: post
thumbnail: /assets/uploads/drag-drop-350.png
date: 2021-05-13T09:05:24.506Z
date-custom: May 13, 2021
title: Pain of Unit Testing with Drag and Drop (With Jest)
tags: technical
image: coffee-blue.jpg
description: My first ever blog post! Reason for blog and a little about me
---
Creating unit tests should be a surefire way of knowing if your component is functioning as it's supposed to. For the most part creating these unit tests can be pretty simple. Clicking on a checkbox and seeing if it's checked is a pretty straight forward. Though how do you something as complex as drag and drop when there's no browser? I ran into this very question and want to explain my process behind it.

## **The Issue**

There are couple of things we should try and understand before we dive in. First, how does our testing framework operate? Second, how does the library we use operate?

The testing framework I am currently utilizing is [testing-library](https://testing-library.com/docs/dom-testing-library/intro). This library is built to test DOM Nodes, through simulation of [JSDOM ](https://github.com/jsdom/jsdom)by [Jest](https://jestjs.io/). What does this mean for us? We have a headless browser that does not support layout.

As far as the library goes, I was personally using[ dnd kit](https://github.com/clauderic/dnd-kit). Dnd kit when dragging with mouse compares the position of each draggable item with each other. 

With those two things laid out, it's clear that testing-library and dnd-kit are going to have a hard time working together. With a headless browser, there's no way to compare positional relationships between each DOM Node. However not all hope is lost.

## Solution #1(Accessibility)

We can take the approach that perhaps we can avoid using the mouse. We could always go the route of using a keyboard. This goes hand in hand with the accessibility rules that exist to assist people with disabilities.

According to the third ARIA rule: 

> All interactive ARIA controls must be usable with the keyboard.
>
> If you create a widget that a user can click or tap or drag or drop or slide or scroll, a user must also be able to navigate to the widget and perform an equivalent action using the keyboard.

Luckily for us dnd kit happens to support multiple input types, such as keyboard.  

Here's a quick, dummy example of what that might look like:

```
it('should drag item in list downwards', async () => {
    const { container, getByText, findByPlaceholderText } = render(<FakeListOfDraggableItems />)
    const reorderButton = within(getByText('Columns')).getByLabelText('Reorder Button')
    //Wrapping with React's act helper function is neccessary: https://github.com/testing-library/react-testing-library/issues/276
    act(() => reorderButton.focus())
    expect(document.activeElement === reorderButton).toBeTruthy()
    fireEvent.keyDown(reorderButton, { key: 'Enter', code: 'Enter' })
    fireEvent.keyDown(reorderButton, { key: 'ArrowDown', code: 'ArrowDown' })
    fireEvent.keyDown(reorderButton, { key: 'Enter', code: 'Enter' })
    epect(logicToCheckItemOrder())
  })
```

## Solution #2 (Another framework)

If you are unable to create a successful test or perhaps lack confidence that your test is performing as it should be perhaps it is best to find another framework. Using [Cypress](https://www.cypress.io/), seems to be the best way to go as of right now with it's browser rendering runs into no issues with running the tests mentioned. 

## **Conclusion**

While I know this is a very specific use case, I hope at least one person can get use out of this.