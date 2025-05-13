# Frontend Mentor - QR code component solution

This is my solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H), a platform that helps improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)

## Overview

### Screenshot

Mobile:

![](./images/Screenshot-mobile.png)

Desktop:

![](./images/Screenshot-desktop.png)

### Links

- [Solution URL](https://www.frontendmentor.io/solutions/qr-code-component-using-flexbox-_Cyj_6LhDq)
- [Live site URL](https://qr-code-component-lilac-chi.vercel.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox

### What I learnt

Although this may _look_ simple, it’s a great first project to focus on the fundamentals and start thinking in reusable components rather than full-page layouts.

I focused on writing readable code that is properly structured and indented by using both a local Prettier installation and the Visual Studio Code extension.

I also made sure my code was semantic and accessible by using landmarks (such as `<main>`), meaningful HTML elements that accurately describe the content and `alt` text that properly describes the image and its purpose.

I learnt how to self-host a variable Google font, convert it from a `ttf` to `woff2` format for better optimisation and write a `@font-face` declaration:

```css
@font-face {
  font-family: "Outfit";
  src: url("./fonts/Outfit-VariableFont.woff2") format("woff2");
  font-weight: 100 900;
  font-display: swap;
}
```

### Useful resources

- [How to write good alt text for screen readers](https://www.craigabbott.co.uk/blog/how-to-write-good-alt-text-for-screen-readers/) - This article by Craig Abbott was shared in Frontend Mentor's Discord as a recommended resource for learning how to write appropriate `alt` text.
- [Self-hosting fonts explained (including Google fonts) // @font-face tutorial](https://www.youtube.com/watch?v=zK-yy6C2Nck&t=66s) and [Getting started with Variable fonts on the web](https://www.youtube.com/watch?v=0fVymQ7SZw0&t=1s) - These two videos from Kevin Powell helped me self-host the Google font and set it up correctly in the project.
