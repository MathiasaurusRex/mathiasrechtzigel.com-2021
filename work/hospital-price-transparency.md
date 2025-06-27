---
title: Helping Hospitals Meet the Hospital Price Transparency Law
description: I prototyped and delivered simple open source prototypes that are estimat
date: 2024-03-01
tags:
  - Public Website
layout: layouts/post.njk
logo: ../img/logo/dsac-stacked.jpg
templateClass: layout-post layout-post-portfolio

url: https://www.mathiasrechtzigel.com/work/988-suicide-and-crisis-lifeline
---

<p class="lead-p">Wouldn’t it be helpful if you could visit a hospital’s website and easily see the prices for services? That’s the goal of the Hospital Price Transparency law. But in practice, the law has been difficult to implement. Hospitals received conflicting guidance from regulators and were left trying to figure it out on their own. That’s where I came in.</p>

## What the law hoped to accomplish

Starting in 2021, every hospital in the United States had to post clear and accessible pricing information online in two ways:
* A machine-readable file with all items and services
* A consumer-friendly list of shoppable services



## Sounds simple, what was the problem?
Many hospitals, especially small or rural ones, were not set up for this. They used basic website builders like Squarespace, Wix, or Webflow. Their priority was patient care, not building complex web tools. Larger organizations could also get caught in a morass due to conflicting opinions from people who were not the authority on the subject.

Through user research with hospitals, billing specialists, and service providers, we identified three main problems:

* <strong>Data confusion</strong>. The law required a "machine-readable" file, but didn’t define what that meant or how machines should read the file.
* <strong>Website limitations</strong>. Hospitals needed to show thousands of services in a user-friendly way, but drag-and-drop site builders made that difficult.
* <strong>Enforcement pressure</strong>. Hospitals wanted to follow the rules, but there was no easy way to check if their files met the standards.

## Our first prototyp: an easy-to-use validator

As any good content strategist knows, you have to make sure that you lead with content first. Content in this context meant formatting the chargemaster to meet the needs of the public. 

To reduce the burden, we built a simple prototype. Hospitals could upload their pricing file and check it against an open-source data dictionary. If their file met the content requirements, they would get immediate confirmation.

I modeled the tool after web-based validators like the WebAIM contrast checker, HTML5 validators, and Lighthouse tools in Chrome. Our goal was to make validation as simple and reliable as possible. This was only one in a series of tools that you can find on the Hospital Price Transparency website.

## Once we had that: a web crawler and validator of our own

Now that we knew that hospitals had the tools to meet their requirements, we could provide some extra guidance on where to place the file and how to format it. We created a new metadata format that would allow hospitals to place their file where they needed it based on their technology constraints. This allowed us to automate our enforcement and we could give hospitals a friendly heads up if we saw something out of sorts.

This would help solve most of the issues related to website limitations, but in cases that it didn't it gave more time and space for our outreach team to hear about the technical edge cases that effected hospitals with lower resources.

## What was our impact?

These tools removed the guesswork. Hospitals could drag and drop their files and instantly know if they were compliant. It also helped rural hospitals confirm that their third-party contractors were doing the job right. Saving both time and money.

<strong>How much time did it save?</strong> We estimated that this simple tool could save hospitals across the country more than 900,000 hours per year.

This was also one of the <a href="https://www.cms.gov/digital-service/transparency#:~:text=Hospital%20price%20transparency%20(HPT)%20helps,pricing%20data%20on%20their%20websites.">Open Source Program Office at the Centers for Medicare and Medicaid Services early wins</a> in being able to point to how open source tools could provide direct impact and savings to the healthcare system.

<strong>See more about this across the web:</strong>
