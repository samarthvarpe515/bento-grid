# Frontend Mentor - Bento grid solution

This is a solution to the [Bento grid challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/bento-grid-RMydElrlOj).

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the interface depending on their device's screen size

### Screenshot

![Bento grid solution on desktop](./screenshot.png)

### Links

- Solution URL: [GitHub repo](https://github.com/samarthVarpe515/bento-grid)
- Live Site URL: [Live site](https://samarthvarpe515.github.io/bento-grid/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- CSS Grid with `grid-template-areas`
- Flexbox
- Fluid typography with `clamp()`
- Mobile-first workflow

### What I learned

**Named grid areas make bento layouts easy to read and change.** The whole desktop layout is visible in one place, and moving a card just means moving its name:

```css
.bento {
  grid-template-columns: repeat(4, 1fr);
  grid-template-areas:
    "create  hero       hero       schedule"
    "write   hero       hero       schedule"
    "write   accounts   consistent schedule"
    "write   faster     grow       grow";
}

```
**Keep source order meaningful.** The HTML follows the mobile reading order, so screen readers and keyboard users get a logical sequence, and CSS Grid rearranges the cards visually on desktop. In the "Grow followers" card, the design puts the image above the heading on mobile. I used `flex-direction: column-reverse` instead of moving the heading below the image in the HTML.

**Fluid type with `clamp()`.** Headings scale smoothly between the 375px and 1440px designs without extra media queries:

```css
--fs-h1: clamp(2.5rem, 1.6rem + 2.5vw, 3.5rem);
```

**Decorative images.** The illustrations repeat what each card's heading already says, so they use `alt=""` and screen readers skip them.

### Continued development

- Matching spacing to the design more precisely at in-between widths
- Adding subtle hover or entrance animations that respect `prefers-reduced-motion`

## Author

- GitHub - [@samarthvarpe515](https://github.com/samarthvarpe515)
- Frontend Mentor - [@samarthvarpe515](https://www.frontendmentor.io/profile/samarthvarpe515)
- LinkedIn - [Samarth Varpe](https://www.linkedin.com/in/samarthvarpe515)