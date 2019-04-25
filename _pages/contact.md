---
layout: default
title: Contact
permalink: /contact/
heading: Contact
subheading: Like what you see? Send me a message
floating-item: ../assets/img/message-in-a-bottle.svg
floating-item-text: floating bottle
floating-item-height: 150px
---

<h2 class="section-title">Send me an email!</h2>
<!-- <p class="text-center text-white py-0 my-0">(Replies within a day)</p> -->
<form id="contact-form" class="row justify-content-between"  name="contact" data-netlify="true" data-netlify-recaptcha="true"> 
    <input type="text" name="name" class="col-md-5 col-lg-5 col-sm-12" placeholder="Name"> 
    <input type="text" name="email" id="email" class="col-md-6 col-lg-6 col-sm-12" placeholder="Email Adress"><br>
    <textarea class="col-12" rows="6" placeholder="Message" name="message"></textarea><br>
    <div data-netlify-recaptcha="true"></div>
    <button type="submit" class="btn btn-outline-light btn-block" id="submit-btn">Send Message</button>
</form>
<h2 class="section-title">Too cool for email?</h2>
<div  id="icons">
    <a href="https://twitter.com/JonathanSouth17" target="_blank">
        <span class="fa-stack fa-2x">
            <i class="fas fa-square fa-stack-2x"></i>
            <i class="fab fa-twitter-square fa-stack-1x fa-inverse"></i>
        </span>
    </a>
    <a href="https://www.linkedin.com/in/jonathan-southern-772b4b135/" target="_blank">
        <span class="fa-stack fa-2x">
            <i class="fas fa-square fa-stack-2x"></i>
            <i class="fab fa-linkedin fa-stack-1x fa-inverse"></i>
        </span>
    </a>
</div>