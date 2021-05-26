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
<!--------------------- CONTACT FORM ----------------------->
<form class="contact-form my-5" name="contact" data-netlify="true"> 
  <div class="row g-2">
    <div class="col mb-3">
      <label class="form-label">Name</label>
      <input type="name" class="form-control">
    </div>
    <div class="col mb-3">
      <label class="form-label">Email address</label>
      <input type="email" class="form-control" aria-describedby="emailHelp">
      <div id="emailHelp" class="form-text">This is so I can respond back to you</div>
    </div>
  </div>
  <div class="form-floating mb-3">
    <textarea class="form-control" placeholder="Leave a comment here" id="messageTextarea" style="height: 100px"></textarea>
    <label for="messageTextarea">Message</label>
  </div>
  <div class="mb-3">
    <input type="file" class="form-control" >
  </div>
  <button type="submit" class="btn btn-light">Send Message</button>
</form>

<!--------------------- OTHER SOCIAL ----------------------->
<h3 class="text-center mb-2">Find me elsewhere </h3>
<div class="row mx-auto mb-5 icons">
  <div class="col-sm text-center">
    <a href="https://www.linkedin.com/in/jonathan-southern-772b4b135/" target="_blank"> 
      <i class="fab fa-linkedin-in"></i>
    </a>
  </div>
  <div class="col-sm text-center">
    <a href="https://stackoverflow.com/users/11380925/jonathan-s" target="_blank"> 
      <i class="fab fa-stack-overflow"></i>
    </a>
  </div>
  <div class="col-sm text-center">
    <a href="https://github.com/JonathanSouthern" target="_blank"> 
      <i class="fab fa-github"></i>
    </a>
  </div>
</div>
