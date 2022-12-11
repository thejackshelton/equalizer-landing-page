# Frontend Mentor - Equalizer landing page solution

This is a solution to the [Equalizer landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/equalizer-landing-page-7VJ4gp3DE). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

A phone app landing page using Mobile First & SASS.

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

- [Project Screenshot](https://imgur.com/iQRhpD0)

### Links

- Solution URL: [Solution URL](https://github.com/thejackshelton/equalizer-landing-page)
- Live Site URL: [Live Site URL](https://equalizer-landing-page-gamma.vercel.app/)

## My process

I began with setting up the base styles and typography, and then converting it to rems using a sass function.

From there I used breakpoint mixins using mobile first to implement the design system.

I also used margin auto and flexbox + position layout modes to style the landing page.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow
- [SASS](https://sass-lang.com/documentation/) - CSS Preprocessor

### What I learned

The main thing I learned from this challenge was how to interact with decorative background images.

I used the ::after psuedo element and background-image, and a bunch of other background related css properties to try and emulate the design.

```css
&::after {
    content: "";
    width: rem(580);
    background-image: url("../assets/bg-main-mobile.png");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: top;
    position: absolute;
    top: rem(-300);
    right: rem(-300);
    height: rem(1000);

    @include breakpoint(tablet) {
      background-image: url("../assets/bg-main-tablet.png");
      width: rem(983);
      height: rem(808);
      right: rem(35);
    }

    @include breakpoint(desktop) {
      background-image: url("../assets/bg-main-desktop.png");
      background-position: top;
      background-repeat: no-repeat;
      width: 120%;
      left: -150px;
      top: -250px;
      height: rem(1700);
    }
```

### Continued development

I'm still not as comfortable as I'd like to be when it comes to using accessible units in different use cases.

I also believe that I used an unnecessary amount of nesting for the app buttons, but I'm not entirely sure.

I look forward to improving my CSS, and am actively playing a role in strengthening my foundation.

Have also noticed an odd scroll container on Safari only.

I've taken some time to start picking up React & Styled Components. It's something that I'm likely to use for some challenges in the future.

### Useful resources

- [MDN](https://developer.mozilla.org/en-US/) - Syntax and usage information for CSS background properties.

## Author

- Website - [Jack Shelton (Currently working on the site)](https://jackshelton.com)
- Frontend Mentor - [@thejackshelton](https://www.frontendmentor.io/profile/yourusername)
- Twitter - [@thejackshelton](https://www.twitter.com/thejackshelton)

## Acknowledgments

Special thanks to Josh Comeau for helping me understand the position layout mode.
