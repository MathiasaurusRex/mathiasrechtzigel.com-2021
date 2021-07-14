---
title: Federal Reserve Bank of Minneapolis
description: This is a post on My Blog about leveraging agile frameworks.
date: 2020-07-04
tags:
  - Public Website
layout: layouts/post.njk
logo: ../img/logo/MNFRB_Logo_LeftAligned_BlueCircle.png
---

<p class="lead-p">How  can you nudge the best and brightest economic organizations in the country?<br> One measurable win at a time.</p>

When I joined the Federal Reserve Bank of Minneapolis in 2019 the the application development group was a year into their <i>Agile Transformation</i>. Unfortunately they lacked a dedicated Front End Development, User Experience and Accessibility resource. That's where I came in: not only could I do the work, but I could pitch and convince executive level sponsors to invest in an accessible, reusable and performant system that could support a 30+ year volume of content that they had to migrate from their legacy system.

## Consistency for thousands of economic papers both new and old.
As an economic research organization the Federal Reserve Bank of Minneapolis publishes A LOT OF PAPERS and suplimentary educational material. With three core personas: <strong>uninformed</strong>, <strong>informed</strong>, and <strong>academic</strong> the Federal Reserve Bank of Minneapolis creates personalized content in service of it's mission of <a href="https://minneapolisfed.org/article/2020/welcome">"Pursuing an economy that works for all of us"</a>.

To support this mission, the Public Affairs team needed a technical and design strategy that would scale for the long term but also ensuring that the solution wouldn't place an additional burden on the content authoring team. This required me a strategy that would ensure that all legacy content (30+ years), current, and future content could adhere to our new design language.

<div class='device-collection'>
  <div class='phone-container'>
    <div class='device phone'>
      <img src="/img/minneapolisfed/article-small.png">
    </div>
  </div>
  <div class='tablet-container'>
    <div class='device tablet'>
      <img src='/img/minneapolisfed/article-medium.png'>
    </div>
  </div>
  <div class='device desktop'>
    <img src='/img/minneapolisfed/article-large.png'>
  </div>
</div>


## Reducing Spin on <i>Red Balloon, Blue Sky</i> Conversations

You have been there. Someone says that you need to change some spacing on the "Card Component". Your developer opens up their fancy design system and low and behold there's four different cards that have different spacing on the four break points that you support. Everyone is crunched for time because you're trying to do more with less (but somehow you always do less with more, isn't that funny?), so your development team makes a quick change and deploys it. Looks good on my machine, ship it.

A couple of weeks later the Creative Director adds a comment to the ticket: "Not seeing this updated. Let me know if you need any help."

Oh no. The developer is far from when they made the change that they can't quite remember <i>what</i> they change, and now they have to make another change. 

<div style="text-align: center;"><strong>Now you've created some visual tech debt.</strong></div>

<div style="font-size: 100px; text-align: center;">🎉🥳🎉</div>

<strong>How can we fix this?</strong> During my time at the Federal Reserve Bank of Minneapolis I created a couple of tools to help reduce this spin. Instead of having our wireframes as pdf's on the server, the names of the components in the design system, and the back end code naming their components in different ways I created a tool based on <a href="https://meyerweb.com/eric/thoughts/2017/11/27/generating-wireframe-boxes-with-css-and-html5/">Eric Meyer's Generating Wireframe Boxes with CSS and HTML5</a> that allowed each and every componenent we created to have a consistent nomenclature across multiple projects and code repositories. 

<p class="lead-p">In short... I baked the wireframes INTO the website, and with a couple lines of CSS and Javascript, anyone could toggle "Wireframe Mode", eliminate spin, and start speaking the same language.</p>


<div class="img-comp-container">
  <div class="img-comp-img">
    <img src="/img/minneapolisfed/wireframe-off.png">
  </div>
  <div class="img-comp-img img-comp-overlay">
     <img src="/img/minneapolisfed/wireframe-on.png">
  </div>
</div>

## Multi-platform Consistency

Responsive design was table-stakes in 2019, now users expect that the content they see is consistent across all of their platforms. Luckily we were able to add a few lines of automated meta tag magic via Sitecore to ensure that when the public shared an article on Linkedin, Twitter, or Facebook that it was consistent across all of the platoforms.

- Screenshot on Linkedin, Twitter, Facebook

## Winning hearts, minds... and budgets


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

initComparisons();

</script>