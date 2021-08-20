---
title: X-Rite
description: I worked with X-Rite and was the first project where I had a major hand in the strategic direction of the design and technical implementation.
date: 2017-01-01
tags:
  - Public Website
layout: layouts/post.njk
logo: ../img/logo/xrite.png
templateClass: layout-post layout-post-portfolio

socialImage: https://www.mathiasrechtzigel.com/img/social/work/social-xrite.png
url: https://www.mathiasrechtzigel.com/work/x-right
---

<p class="lead-p">X-Rite was the first project where I had a major hand in the strategic direction of the design and technical implementation from pre-sale to post-launch. Not only did we establish a design system that was flexible to the international content needs of the premier supplier of color calibration technology in the world, I ensured that the system would be able to adapt to the needs of Pantone's color of the year marketing push. </p>

<div class='device-collection'>
  <div class='phone-container'>
    <div class='device phone'>
      <img src="/img/xrite/purple-small.png" alt="X-Rite's purple theme on mobile">
    </div>
  </div>
  <div class='tablet-container'>
    <div class='device tablet'>
      <img src='/img/xrite/purple-medium.png' alt="X-Rite's purple theme on tablet">
    </div>
  </div>
  <div class='device desktop'>
    <img src='/img/xrite/purple-large.png' alt="X-Rite's purple theme on desktop">
  </div>
</div>

## Color Customization

Pantone's color of the year is an extremely fun way for them to market their Color Matching System. A lot of effort goes into studying what might be the "Hot new color" of the year and all of Pantone's partner organizations love to align themselves behind that vision.

From the start, we knew that we wanted to create a system that was simple enough to deploy change in color scheme without having to reconfigure an entire code base. We created a system of SASS variables that could easily be updated within Sitecore so that they content author their changes rather than do a code deployment.

<img src="/img/xrite/pantone-green.jpeg" alt="Pantone Color of the Year 2017 -- Greenery 15-0343!"/>

<div class='device-collection'>
  <div class='phone-container'>
    <div class='device phone'>
      <img src="/img/xrite/green-small.png" alt="X-Rite's green theme on mobile">
    </div>
  </div>
  <div class='tablet-container'>
    <div class='device tablet'>
      <img src='/img/xrite/green-medium.png' alt="X-Rite's green theme on tablet">
    </div>
  </div>
  <div class='device desktop'>
    <img src='/img/xrite/green-large.png' alt="X-Rite's green theme on desktop">
  </div>
</div>

## Internationalization

Managing personalized content within Sitecore is a breeze, which makes it the perfect solution to manage X-Rite's fourteen language Global Gateway.

X-Rite is a global leader of color calibrators. If you're say... Coca-cola... you want to ensure that every single bottle and can you produce is Coca-cola red. You've invested billions of dollars into your brand and you don't want that spoiled because the ambient temperature in a location causes one of the dyes to be a tad bit lighter.

<p class="lead-p" style="text-align: center">You need 'Coca-cola Red',<br>not<br> 'Cola-cola Almost Red'.</p>

We leveraged Sitecore's internationalization engine to ensure that all of the Globally Unique Identifiers could be updated to both region and language appropriate copy. This provided some interesting design challenges. In German "About" transforms into "Informationen" which takes up some extra space in the header. Leveraging some flexible grid systems throughout the website we were able to ensure that every language could respond appropriately to our users screens.

<div class="img-comp-container">
  <div class="img-comp-img">
    <img src="/img/xrite/internationalization-english.png" alt="Screenshot of the mega-navigation in english"/>
  </div>
  <div class="img-comp-img img-comp-overlay">
     <img src="/img/xrite/internationalization-spanish.png" alt="Screenshot of the mega-navigation in spanish"/>
  </div>
</div>

## Building interactive experiences that drive traffic.

In order to drive traffic to the site, we built a responsive Color Challenge and Hue Test. One in 255 women and One in 12 men have some form of color vision deficiency. This interactive page served as an educational item that professionals who work with color could take to prove their mettle.

And they could send it to their bosses, friends, and colleagues. If those folks didn't do so hot, maybe your monitor isn't calibrated correctly and you can purchase a <a href="https://www.xrite.com/categories/calibration-profiling/i1display-pro">i1 Display Pro</a> which is the perfect combination of unrivaled color precision, speed and controls for the highest level of on-screen color accuracy.

As of July 2021 this simple page has had over 378,000 shares.

<img src="/img/xrite/xrite-color-challenge.png" alt="Screenshot of the X-Rite Color Challenge with over 378,000 shares."/>

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
  .img-comp-container {
    height: 600px;
  }
</style>
