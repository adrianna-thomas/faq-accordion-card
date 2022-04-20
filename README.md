# Frontend Mentor - FAQ accordion card solution

This is a solution to the [FAQ accordion card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/faq-accordion-card-XlyjD0Oam). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

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

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the component depending on their device's screen size
- See hover states for all interactive elements on the page
- Hide/Show the answer to a question when the question is clicked

### Screenshot

![](./screenshot.jpg)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

I learned how to make the accordion menu appearance match the design and prevent the image from being stretched out.

```css
.question {
  display: flex;
  justify-content: space-between;
  cursor: pointer;
}

.question img {
  align-self: center;
}
```

I learned how to change the display of certain images depending on the media query screensize. Also learned how to make an image appear on top of another image.

```css
.desktop-image,
.box-image {
  display: inline-flex;
}
.desktop-image {
  position: relative;
  top: -10.5rem;
  left: -4rem;
  z-index: 1;
}
.box-image {
  position: relative;
  top: 5rem;
  left: -5rem;
  z-index: 3;
}
```

I learned how to toggle an active class and apply the style. Also made the accordion arrow change positioning when active.

```js
this.classList.toggle("active");
```

```css
.active p.question-text {
  color: var(--Very-dark-desaturated-blue);
  font-weight: 700;
}

.active img {
  transform: rotate(180deg);
}

.accordion.active .answer-text {
  height: 100%;
}
```

### Continued development

Still unsure on how to insert background images inside the div container like I saw in other solutions. Instead I added them to the html and changed the visibility dependent on screensize.

I also am unsure how to get the card background to appear like the design, the edge of the image crops at the end of the div container and the box moves when adjusting the screensize.

### Useful resources

- [Pixels to Rem Converter](https://www.ninjaunits.com/converters/pixels/pixels-rem/) - This helped me with deciding which rem values to apply to my stylesheet.
- [FreeCodeCamp Article](https://www.freecodecamp.org/news/build-an-accordion-menu-using-html-css-and-javascript/) - This helped me with toggling the answer text in the accordion.
- [StackOverflow Thread](https://stackoverflow.com/questions/48474/how-do-i-position-one-image-on-top-of-another-in-html) - This helped me with making the box image appear on top of the desktop image.

## Author

- Frontend Mentor - [@adrianna-thomas](https://www.frontendmentor.io/profile/adrianna-thomas)

## Acknowledgments

This is where you can give a hat tip to anyone who helped you out on this project. Perhaps you worked in a team or got some inspiration from someone else's solution. This is the perfect place to give them some credit.
