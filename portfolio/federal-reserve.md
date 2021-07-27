---
title: Federal Reserve Bank of Minneapolis
description: From 2019 to 2021 Mathias Rechtzigel worked at the Federal Reserve Bank of Minneapolis and built internal and external websites and applications.
date: 2020-07-04
tags:
  - Public Website
layout: layouts/post.njk
logo: ../img/logo/MNFRB_Logo_LeftAligned_BlueCircle.png
templateClass: layout-post layout-post-portfolio
---

<p class="lead-p">The Federal Reserve Bank of Minneapolis is one of twelve Federal Reserve Banks. When I joined in 2019 they were kicking off a reimagining of how they would serve the public. At the center of this rebranding was the tagline: "Pursing an economy that works for all of us."</p>

In 2019 the application development group was a year into their <i>Agile Transformation</i>. They identified a gap in a dedicated Front End Development, User Experience and accessibility resource. 

That's where I came in. I hit the ground running my first week: identified gaps within approved technologies that we could use to build out the Minneapolis Fed's first design system. I created partnerships between departments that rarely talked to each other and emphasised the importance of user-centered design. Finally being a consultant to our executive level sponsors to invest in an accessible, reusable and performant system that could support a 30+ year volume of content that they had to migrate from their legacy system.

During the completion of the project, they could point to deliverables that extended beyond the project. A design system wasn't just contained to the public website, it could be leveraged across our entire portfolio of internal applications (with some minor tweaks, you don't need big bold marketing fonts on internal data applications). Soon I was able to spin out proof of concept websites with real code in less than a day. Gaining budget and approval to expand the team for larger application initiatives.

It wasn't just a pie in the sky dream. With a decade of experience delivering responsive and flexible websites that could easily be modified based on the needs of our stakeholders. 

## Consistency for thousands of economic papers both new and old.
As an economic research organization the Federal Reserve Bank of Minneapolis publishes A LOT OF PAPERS and supplementary educational material. With three core personas: <strong>uninformed</strong>, <strong>informed</strong>, and <strong>academic</strong> the Federal Reserve Bank of Minneapolis creates personalized content in service of its mission of <a href="https://minneapolisfed.org/article/2020/welcome">"Pursuing an economy that works for all of us"</a>.

To support this mission, the Public Affairs team needed a technical and design strategy that would scale for the long term but also ensuring that the solution wouldn't place an additional burden on the content authoring team. This required a strategy that would ensure that all legacy content (30+ years), current, and future content could adhere to our new design language.

<div class='device-collection'>
  <div class='phone-container'>
    <div class='device phone'>
      <img src="/img/minneapolisfed/article-small.png" alt="Article template on Mobile">
    </div>
  </div>
  <div class='tablet-container'>
    <div class='device tablet'>
      <img src='/img/minneapolisfed/article-medium.png'  alt="Article page on medium">
    </div>
  </div>
  <div class='device desktop'>
    <img src='/img/minneapolisfed/article-large.png'  alt="Article page on desktop">
  </div>
</div>


## Reducing Spin on <i>Red Balloon, Blue Sky</i> Conversations

You have been there. Someone says that you need to change some spacing on the "Card Component". Your developer opens up their fancy design system and low and behold there's four different cards that have different spacing on the four breakpoints that you support. Everyone is crunched for time because you're trying to do more with less (but somehow you always do less with more, isn't that funny?), so your development team makes a quick change and deploys it. Looks good on my machine, ship it.

A couple of weeks later the Creative Director adds a comment to the ticket: "Not seeing this updated. Let me know if you need any help."

Oh no. So much time has passed since the developer has made the change that they can't quite remember <i>what</i> they changed, and now they have to make another change.

All design debt is technical debt and it's important to manage it upfront then letting changes cascade into the future where the easiest way to fix the issue would be to start from scratch. 

<strong>How can we fix this?</strong> During my time at the Federal Reserve Bank of Minneapolis I created a couple of tools to help reduce this spin. Instead of having our wireframes as pdf's on the server, the names of the components in the design system, and the back end code naming their components in different ways I created a tool based on <a href="https://meyerweb.com/eric/thoughts/2017/11/27/generating-wireframe-boxes-with-css-and-html5/">Eric Meyer's Generating Wireframe Boxes with CSS and HTML5</a> that allowed each and every component we created to have a consistent nomenclature across multiple projects and code repositories. 

<p class="lead-p">In short... I baked the wireframes INTO the website, and with a couple lines of CSS and Javascript, anyone could toggle "Wireframe Mode", eliminate spin, and start speaking the same language. Designers could more easily communicate with back end developers and it reduced gaps between teams.</p>


<div class="img-comp-container">
  <div class="img-comp-img">
    <img src="/img/minneapolisfed/wireframe-off.png" alt="Example of Minneapolisfed.org with the wireframe mode turned on.">
  </div>
  <div class="img-comp-img img-comp-overlay">
     <img src="/img/minneapolisfed/wireframe-on.png" alt="The same example of Minneapolisfed.org with the wireframe mode turned off." >
  </div>
</div>

## Multi-platform Consistency

Responsive design was table-stakes in 2019, now users expect that the content they see is consistent across all of their platforms. Luckily we were able to add a few lines of automated meta tag magic via Sitecore to ensure that when the public or one of our partners shared an article on Linkedin, Twitter, or Facebook it would use our branded images.

In addition, this allowed our social media professionals to spend less time wrangling images, tiles, and descriptions and more time focusing on a long-term content strategy. More with less and being good stewards of the public funds.

<img src="/img/minneapolisfed/social-1.png" alt="Image of a MinneapolisFed.org website shared by the Boston Fed, with all branding on Twitter."/>

<img src="/img/minneapolisfed/social-2.png" alt="Image of a MinneapolisFed.org website shared by the Minneapolis Fed, with all branding on Linkedin."/>

## Winning hearts, minds...<br> and budgets

We launched <a href="https://minneapolisfed.org">Minneapolisfed.org</a> eight months after I joined. It was like having chewbacca in the pilot seat and telling him to punch it. During and after this project I was assigned to larger and increasingly ambitious projects.

<ul>
  <li>I conducted technology forecasting that set the direction for a 20+ person technology team.
  </li>
  <li>Highlighted and defined a headless content strategy that would leverage Sitecore 9.3's JSS functionality.</li>
  <li>Pitched and acquired funding for a Customer Experience and User Experience team, to support the Treasury Department that was comprised of User Experience Architects, Researchers, Technologists and Product Designers</li>
  <li>Lead the procurement and security vetting process on a suite of tools to support secure usability testing with the public</li>
  <li>..and much more!</li>  
</ul>

But most of all, working within the Federal Reserve Bank of Minneapolis gave me a greater appreciation for public service at all levels of government. There are some extremely talented folks out there who are making sure that the government is running smoothly. It was an honor to work alongside them.

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