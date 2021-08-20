---
title: United Healthcare
description: In 2019 Mathias Rechtzigel partnered with United Healthcare to build a suite of accessible games.
date: 2019-01-01
tags:
  - Public Website
layout: layouts/post.njk
logo: ../img/logo/united-health.png
templateClass: layout-post layout-post-portfolio

socialImage: https://www.mathiasrechtzigel.com/img/social/work/social-uhc.png
url: https://www.mathiasrechtzigel.com/work/united-health-care
---

<p class="lead-p">United Healthcare partnered with Pixelfarm to build out an interactive game center for their users. They needed the games to meet or exceed the guidelines set forth by the Web Content Accessibility Guidelines(WCAG) so that they could adhere to the American's with Disabilities Act. <br><br>So I built out some amazing, accessible, and responsive web games. How cool is that?</p>

## Game Center

The hub of all the games needed to showcase everything that United Healthcare could offer. All of the games were reviewed and were tagged with appropriate considerations. Some games has special considerations for screen reader support, keyboard-only play, difficulty selection, and vertical only support. This allowed folks who might have cognitive, visual, and motor impairments to better control how they would like to play.

In total we had six games: Memory Recall, Word Scramble, Shuffle Club (a Breakout clone), a Jigsaw Puzzle, Party Pop (a simple match game), and Trivia Casino!

<img src="/img/uhc/gc-main.png" alt="Screenshot of the Game Center's main screen that highlights six web games."/>
<img src="/img/uhc/gc-a11y.png" alt="Screenshot of the Game Center's accessibility dropdown that showcases checkboxes to filter games based on screen reader support, keyboard-only play, difficulty selection, and vertical only mobile support."/>

## Memory Recall

Building a memory recall game to meet WCAG is a tricky proposition because most screen readers allow you to replay the content that is read to you.

The first iteration was using an aria-live region and having the cards announce their numbers on animation. Unfortunately after some play testing with users we discovered that most of them would replay the sequence and quickly type it in.

So we purposely decided to _degrade_ the experience so that they had the same game experience as folks who weren't using assistive technology. We did this by creating custom audio cues! Fun!

<div class='device-collection'>
  <div class='phone-container'>
    <div class='device phone'>
      <img src="/img/uhc/gc-cr-small.png" alt="">
    </div>
  </div>
  <div class='tablet-container'>
    <div class='device tablet'>
     <img src="/img/uhc/gc-cr-medium.png" alt="">
    </div>
  </div>
  <div class='device desktop'>
    <img src="/img/uhc/gc-cr-large.png" alt="">
  </div>
</div>

## Trivia Casino

Building a fully accessible trivia game is a tad bit easier. We were still using custom audio cues for aesthetic reasons but the main accessibility challenge here was that the original version was timed.

A timed game makes it challenging for folks who might have cognitive disabilities to play the game to their full enjoyment. After some conversations it was decided that while a "timed" version might be more challenging, it didn't actually add anything to the game.

<div class='device-collection'>
  <div class='phone-container'>
    <div class='device phone'>
      <img src="/img/uhc/gc-tc-small.png" alt="">
    </div>
  </div>
  <div class='tablet-container'>
    <div class='device tablet'>
     <img src="/img/uhc/gc-tc-medium.png" alt="">
    </div>
  </div>
  <div class='device desktop'>
    <img src="/img/uhc/gc-tc-large.png" alt="">
  </div>
</div>

## Technical Considerations

Each game allowed their players to collect "coins" that they could then use to unlock special skins, new games, and other fun goodies.

To manage this centrally we leveraged Firebase to store the players custom ID and the progress they made and each game was hosted in a custom build React wrapper that managed state and personalization across the multiple applications.
