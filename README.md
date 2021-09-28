# Frontend Mentor - Meet landing page solution

This is a solution to the [Meet landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/meet-landing-page-rbTDS6OUR). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](./meet-landing-page/assets/screenshot.jpg)

### Links

- Live Site URL: [https://gchristofferson.github.io/meet-landing-page/](https://gchristofferson.github.io/meet-landing-page/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

During this first project I completed on Frontend Mentor, I wanted to practice CSS Grid a little more, as I have done several previous projects creating layouts with flexbox and haven't really had an opportunity to hone my skills using Grid. I really enjoyed how easy it was to edit layouts for different screens simply by rearranging the grid-template-areas or reassigning elements to different grid areas.

See how I made the hero section responsive on mobile and desktop by changing the grid-template-columns and grid-template-areas in my example below.  First the HTML:

```html
<section class="hero">
  <div class="hero__img img-left">
    <img src="./assets/desktop/image-hero-left.png" alt="hero image">
  </div>
  <div class="hero__img img-right">
    <img src="./assets/desktop/image-hero-right.png" alt="hero image">
  </div>
  <div class="hero__img">
    <img src="./assets/tablet/image-hero.png" alt="hero image">
  </div>
  <div class="hero__content">
    <h1 class="hero__title">Group Chat <span>for Everyone</span></h1>
    <p class="hero__text body-text">Meet makes it easy to connect with others face-to-face virtually and collaborate across any device.</p>
    <button class="btn">Download <span>v1.3</span></button>
    <button class="btn btn--secondary btn--small">What is it?</button>
  </div>
</section>
```
Next, the mobile-first css:
```css
.hero {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    align-content: center;
    overflow: hidden;
    margin-bottom: calc(4rem + 84px);
    grid-template-areas: "h-img     h-img     h-img     h-img"
                         "h-content h-content h-content h-content"

}
```
I assigned .hero__img to 'h-img' grid area, while I set .img-left and .img-right to display:none. Then I assigned .hero__content to the 'h-content' grid area. For the desktop layout (min-width: 1300px) I changed the grid-template-areas and grid-template-columns.
```css
@media (min-width: 1300px) {
  .hero {
    grid-template-columns: 1fr 2fr 1fr;
    grid-template-areas: "h-img-l h-content h-img-r";
    overflow: visible;
    min-height: 358px;
    margin-bottom: calc(7rem + 94px);
  }
}
```
I assigned .img-left to 'h-img-l' and .img-right to 'h-img-r' while .hero__img was set to display:none.  This is the only way I currently know how to switch the display of the single image used for the mobile and tablet layouts to the split image with the text in the center for the desktop layout.  I don't know if this is the best solution but I did like out Grid made it very easy to make these adjustments.  

I also learned a lot about writing markdown and a good README.md document, thanks to the help from Frontend Mentor!

### Continued development

Use this section to outline areas that you want to continue focusing on in future projects. These could be concepts you're still not completely comfortable with or techniques you found useful that you want to refine and perfect.

In future projects I want to focus on refining my use of measurements.  I want to learn the best practices for using ems vs. rems.  I know some developers use ems for breakpoints and padding and rems for everything else.  I found that using rems for font-size and margins worked well in this project but I'm not 100% sure this is the best.  Also, I will be diving more into JavaScript in future projects and using CSS animations and transitions.

## Author

- Frontend Mentor - [@gchristofferson](https://www.frontendmentor.io/profile/gchristofferson)
