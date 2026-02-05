# Frontend Mentor - QR code component solution

This is a solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H).

## Table of contents

- [Overview](#overview)
  - [Screenshots](#screenshots)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)

## Overview

### Screenshots

Mobile:

![mobile screenshot](/assets/images/screenshots/mobile-screenshot.jpeg)

Desktop:

![desktop screenshot](/assets/images/screenshots/desktop-screenshot.jpeg)

### Links

- [Solution URL](https://www.frontendmentor.io/solutions/qr-code-component-dZ5Xzi3b3Q)
- [Live site URL](https://qr-code-component-dionysialemonaki.vercel.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox

### What I learned

I learned about landmarks, and how every page needs to at least have a `main` landmark to represent its primary content. I also used an `article` element for the QR code card because this represents self-contained content that makes sense on its own, and gave it an accessible name with `aria-labelledby`.

```html
<main>
  <article aria-labelledby="frontend-mentor-qr-code">
    ...
    <h2 id="frontend-mentor-qr-code">
      Improve your front-end skills by building projects
    </h2>
    ...
  </article>
</main>
```

For the image, I provided descriptive alt text that clearly conveys its purpose to screen readers, along with `width` and `height` attributes to prevent layout shift.

```html
<img
  src="/assets/images/image-qr-code.png"
  alt="QR code to frontendmentor.io"
  width="288"
  height="288"
/>
```

I learned how to self-host a variable font and about converting it from a `.ttf` to `woff2` format and adding `font-display: swap` for better performance.

```css
@font-face {
  font-family: "Outfit";
  font-style: normal;
  font-weight: 100 900;
  font-display: swap;
  src: url("/assets/fonts/Outfit-VariableFont.woff2") format("woff2");
}
```

Lastly, I learned about avoiding fixed widths and heights. For the component, I used a `max-width` instead of a fixed `width` to let the component grow up to the specified size but also allow it to shrink when needed, such as on mobile screens. When it came to centering it on the screen, I used `min-height: 100vh` on the `body`, since by default the `body` is only as tall as its content. This ensures the page is at least as tall as the viewport and prevents content from being cut off on smaller screens.
