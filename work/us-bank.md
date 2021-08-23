---
title: U.S. Bank
description: From 2018 to 2019 Mathias Rechtzigel worked at U.S. Bank, building their first design system and ensuring that Super Bowl projects were accessible.
date: 2018-01-01
tags:
  - Public Website
layout: layouts/post.njk
logo: ../img/logo/USBank.png
templateClass: layout-post layout-post-portfolio

socialImage: https://www.mathiasrechtzigel.com/img/social/work/social-usb.png
url: https://www.mathiasrechtzigel.com/work/us-bank
---

<p class="lead-p">It's the end of 2017, and The Big Game is coming to Minneapolis at the beginning of 2018. Hosted at U.S. Bank Stadium. With a Nielsen Rating of 43.1 and an average of 106 million viewers. <br><br>This meant a lot of high profile projects needed to be aligned to our new brand and exceed the Web Content Accessibility Guidelines. </p>

## New Homepage

When you have that many viewers that might potentially hit your homepage and you want to get everything above the fold? Well, you build a carousel. Not just ANY carousel. A personalized carousel. A personalized carousel that was one of the most accessible carousels on the planet on such a high profile website. We ticked every box back in 2018. You could:

<ul>
  <li>Pause and play the auto rotation</li>
  <li>Delete Slides</li>
  <li>Navigate through with tabs, arrows, access keys, voice commands</li>
</ul>

And it was all built with vanilla HTML, CSS, and Javascript. With the amount of traffic that we were expecting, we needed to keep the webpage light and so that we personalize the content through our Adobe Target account and connect to other API's to continue to let folks log into their accounts.

You heard that right folks, hand-crafted, bespoke, web code, no fancy added libraries. Yo' momma didn't raise no fool.

We actually uncovered a bug with VoiceOver when you would lock a viewport to 100vh and with dynamic and personalized content and sent it over to some accessibility engineers over at Apple to document.

<img src="/img/usbank/usb-homepage.jpeg" alt="Screenshot of the Game Center's main screen that highlights six web games."/>

## The quickest of wins for Online Banking

Our Online Banking portal was still using a slightly outdated brand. The trouble was that our technology partners had estimated that it would not be able to be done before our code-freeze date to make it in time for the Superbowl. I raised my hand, rolled up my sleeves and got to work.

I snagged the HTML, CSS and Javascript from online banking and created a local environment the replicated the development environment of our technology partners. This allowed me to work, and deploy changes without the overhead of the entire devops pipeline. Unfortunately I wasn't able to touch the HTML, but the CSS was fair game.

So anyway...I started blasting the CSS and rebuilt it from scratch (and throwing in some media queries and additional vanilla javascript to manage some tasty mobile hamburger navigations for bonus points), we were able to launch a slightly updated branding of our Online Banking portal just in time.

<div class="img-comp-container">
  <div class="img-comp-img">
    <img src="/img/usbank/usb-newolb.png" alt="U.S. Bank's Online Banking circa 2018">
  </div>
  <div class="img-comp-img img-comp-overlay">
     <img src="/img/usbank/usb-oldolb.png" alt="U.S. Bank's Online Banking before 2018">
  </div>
</div>

## One Button, Two Button, Red Button, Blue Button

After rebuilding little pieces of projects with vanilla HTML, CSS and Javascript I had a nice start to a hand coded design system. We had a significant amount of documentation within Invision but I was able to hand off reusable and WCAG 2.1 AA compliant code (I sat right next to some very gracious native screen reader users that I love dearly) to our technology partners.

There were a lot of designers, and a lot of disparate versions of elements that looked _close_ but not _exact_. I worked with a lot of visual designers and user experience professionals to help them better understand the grain of the web, how inline, block, margin collapse, line height affecting the box model, and all that good stuff that caused major headaches.

The culmination of the HTML can be found in places across the public marketing site, consistently sized buttons are my mark. Unfortunately the design system I worked on was lost to time, but shortly there-after the Omnichannel User Experience team launched <a href="https://shield.usbank.com/">Shield</a>, but if you ever see a CSS class that has an override and is prepended with "mr-" you know that's me!

<script>
function initComparisons() {
  var x, i;
  /* Find all elements with an "overlay" class: */
  x = document.getElementsByClassName("img-comp-overlay");
  for (i = 0; i < x.length; i++) {
    /* Once for each "overlay" element:
    pass the "overlay" element as a parameter when executing the compareImages function: */
    compareImages(x[i]);
  }
  function compareImages(img) {
    var slider, img, clicked = 0, w, h;
    /* Get the width and height of the img element */
    w = img.offsetWidth;
    h = img.offsetHeight;
    /* Set the width of the img element to 50%: */
    img.style.width = (w / 2) + "px";
    /* Create slider: */
    slider = document.createElement("DIV");
    slider.setAttribute("class", "img-comp-slider");
    /* Insert slider */
    img.parentElement.insertBefore(slider, img);
    /* Position the slider in the middle: */
    slider.style.top = (h / 2) - (slider.offsetHeight / 2) + "px";
    slider.style.left = (w / 2) - (slider.offsetWidth / 2) + "px";
    /* Execute a function when the mouse button is pressed: */
    slider.addEventListener("mousedown", slideReady);
    /* And another function when the mouse button is released: */
    window.addEventListener("mouseup", slideFinish);
    /* Or touched (for touch screens: */
    slider.addEventListener("touchstart", slideReady);
     /* And released (for touch screens: */
    window.addEventListener("touchend", slideFinish);
    function slideReady(e) {
      /* Prevent any other actions that may occur when moving over the image: */
      e.preventDefault();
      /* The slider is now clicked and ready to move: */
      clicked = 1;
      /* Execute a function when the slider is moved: */
      window.addEventListener("mousemove", slideMove);
      window.addEventListener("touchmove", slideMove);
    }
    function slideFinish() {
      /* The slider is no longer clicked: */
      clicked = 0;
    }
    function slideMove(e) {
      var pos;
      /* If the slider is no longer clicked, exit this function: */
      if (clicked == 0) return false;
      /* Get the cursor's x position: */
      pos = getCursorPos(e)
      /* Prevent the slider from being positioned outside the image: */
      if (pos < 0) pos = 0;
      if (pos > w) pos = w;
      /* Execute a function that will resize the overlay image according to the cursor: */
      slide(pos);
    }
    function getCursorPos(e) {
      var a, x = 0;
      e = e || window.event;
      /* Get the x positions of the image: */
      a = img.getBoundingClientRect();
      /* Calculate the cursor's x coordinate, relative to the image: */
      x = e.pageX - a.left;
      /* Consider any page scrolling: */
      x = x - window.pageXOffset;
      return x;
    }
    function slide(x) {
      /* Resize the image: */
      img.style.width = x + "px";
      /* Position the slider: */
      slider.style.left = img.offsetWidth - (slider.offsetWidth / 2) + "px";
    }
  }
}


if(document.documentElement.scrollWidth > 1000) {
  initComparisons();
}
</script>

<style>
  @media(min-width: 1000px) {
    .img-comp-container {
        width: calc(100% + 600px);
        height: 830px;
        position: relative;
        margin-left: -300px;
        margin-right: -300px;
        margin-top: 50px;
        margin-bottom: 50px;
        box-shadow: var(--box-shadow);
      }
  }
</style>
