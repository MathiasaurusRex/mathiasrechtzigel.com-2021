---
title: Keeping Emergency Rooms safe in the United States.
description: In 2024 I led the the first public EMTALA complaint portal, helping to double enforcement and expanding ER rights through trauma-informed, accessible design.
date: 2024-05-01
tags:
  - Public Website
layout: layouts/post.njk
logo: ../img/logo/CMSlogo.png
templateClass: layout-post layout-post-portfolio

socialImage: https://www.mathiasrechtzigel.com/img/social/work/social-usb.png
url: https://www.mathiasrechtzigel.com/work/emergency-medical-treatment-and-labor-act
---

<p class="lead-p">After the Supreme Court overturned Roe v. Wade in June 2022, the federal government needed a way to protect people seeking emergency care. Especially in states where reproductive health access was changing quickly. </br></br> I was tasked to lead the design and facilitate new opportunities for people living in America.</p>

<p>
  One of the strongest tools was <strong>EMTALA</strong>, the Emergency Medical Treatment and Labor Act. It requires nearly every hospital in the U.S. to do three things in an emergency department:
</p>
<ol>
  <li>Give you a medical screening exam</li>
  <li>Stabilize your emergency condition</li>
  <li>Or transfer you safely if they can’t treat you</li>
</ol>

<p>
  While the headlines focused on abortion care, our research revealed something broader: EMTALA protections mattered for many communities. This included people denied care due to race, addiction history, disability, or lack of insurance.
</p>

<p><strong>Here are some examples of what EMTALA violations can look like:</strong></p>
<ul>
  <li>
    A patient shows up at the emergency room and is turned away because of their race. The hospital does not examine them. That is a violation of EMTALA.
  </li>
  <li>
    A patient with a history of opioid use comes in with a medical emergency. The hospital refuses to treat them because of their addiction. That is a violation of EMTALA.
  </li>
  <li>
    A hospital sends a patient to another facility, not because they cannot treat the person, but because they do not want to lose money. This is called patient dumping. If the transfer is not safe or medically necessary, it is a violation of EMTALA.
  </li>
</ul>

<h2>The challenge with these types of laws</h2>
<p>
  There was no clear or public way for patients or providers to report EMTALA violations. The existing complaint system was buried in legacy government tech and only accessible by phone or email. People also had to know exactly how the law applied to their circumstances – and many were afraid to come forward at all, especially in an environment where the very place they were reporting (States, Hospitals) could be the very group that was violating their rights. This caused a significant underreporting of EMTALA violations.
</p>

<h2>Doing what we could to keep the public safe</h2>
<p>
  I led the design of a public-facing EMTALA complaint portal and educational resources for the public. The first of its kind. It gave anyone in the U.S. a simple, secure way to share what happened in an ER. If the story pointed to a possible EMTALA violation, it would automatically trigger a state-level investigation.
</p>
<p>We focused on making the tool and resources:</p>
<ul>
  <li>Anonymous by default</li>
  <li>Accessible across devices</li>
  <li>Understandable in plain language</li>
</ul>

<h2>Modernizing legacy systems to make it more accessible to everyday people</h2>
<p>
  Behind the scenes, we connected to a backend system called ASPEN, which routes cases to state survey agencies that investigate hospitals. That infrastructure worked, but it was old and had never been made available to the public before.
</p>
<p>
  &lt;screenshot of aspect&gt; - You can actually see guides of the ASPEN portal online. Not very user friendly, but the professionals knew it like the back of their hand.
</p>
<p>
  To bridge that gap, I worked across CMS, HHS, and the White House’s Office of Information and Regulatory Affairs to create a trauma-informed, four-question form that avoided government jargon:
</p>
<ol>
  <li>Would you like to provide contact information or file anonymously?</li>
  <li>What is your relationship to the patient?</li>
  <li>Let us know where the problem happened?</li>
  <li>Tell us what happened?</li>
</ol>

<p>
  We tested the form with advocacy groups, patients, and frontline organizations to make sure it was easy to use. Because for some people they may be in distress or navigating trauma for one of the worst days of their life. We wanted to make sure that this was as simple as possible… because it truly mattered.
</p>
<p>Another goal was that the average person could submit an issue in under 5 minutes. We wanted to reduce the administrative burden as much as possible and shift the burden onto the government.</p>
<p>&lt;Image of educational resources&gt; / &lt;Image of Form&gt;</p>

<h2>Impact</h2>
<p>
  This work brought EMTALA protections to life for the public, and not just for lawyers and regulators. It gave patients and providers a real path to report harm, anonymously if needed, and helped federal agencies respond more quickly to civil rights violations in emergency rooms. In the first 5 months of 2024, we saw double the increase of enforcement actions from 2022.
</p>

<h3>Reporting across the web:</h3>
<ul>
  <li>
    <a href="https://www.washingtonpost.com/health/2024/05/21/emergency-abortions-health-care-emtala/" target="_blank"><strong>Denied emergency health care?</strong> Feds pledge to expedite patient complaints.</a> May 21, 2024 – <em>Washington Post</em>
  </li>
  <li>
    <a href="https://www.medpagetoday.com/opinion/second-opinions/110719#:~:text=Why%20is%20this%20the%20case,other%2C%20for%20fear%20of%20retaliation." target="_blank"><strong>CMS Is Making It Easier to Report EMTALA Complaints.</strong> Here's What Might Change.</a> –  June 19, 2024 <em>MedPageToday</em>
  </li>
</ul>
</section>

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
