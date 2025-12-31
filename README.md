# Frontend Mentor - QR code component solution

This is my solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H).

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

![Mobile version of the QR code component](/assets/images/screenshots/mobile-screenshot.jpeg)

Desktop:

![Desktop version of the QR code component](/assets/images/screenshots/desktop-screenshot.jpeg)

### Links

- [Solution URL](https://www.frontendmentor.io/solutions/qr-code-component-WPxToOWOyE)
- [Live site URL](https://qr-code-component-dionysialemonaki.vercel.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- CSS logical properties
- Self-hosted variable fonts
- Flexbox

### What I learned

For the HTML, I focused on writing well-formatted and consistently indented code using Prettier, both through a local installation and the Visual Studio Code extension. I also added a formatting script to `package.json`:

```json
 "scripts": {
    "format": "prettier --write \"**/*.{css,html}\""
  },
```

I used the `main` landmark for the primary content and the `article` element for the card because it is self-contained and makes sense on its own. I also used `aria-labelledby` to reference the `h2` heading, giving the `article` an accessible name.

```html
<article aria-labelledby="qr-code-frontendmentor">
  ....
  <h2 id="qr-code-frontendmentor">
    Improve your front-end skills by building projects
  </h2>
  ....
</article>
```

For the image, I provided descriptive alt text that clearly conveys its purpose to screen readers, along with `width` and `height` attributes to prevent layout shift.

In the CSS, I first checked for color contrast issues and verified that the colors meet WCAG AA criteria by using the [Polypane Color contrast checker](https://colorcontrast.app/#fg=%23107db5&bg=%23fff&level=aa&format=rgb&algo=WCAG2&filter=none) and then converted the Figma design system into custom properties declared in the `:root`.

I also self-hosted a variable font after converting it from a `.ttf` to a `.woff2` format and added `font-display: swap;` for better performance:

```css
@font-face {
  font-family: "Outfit";
  src: url("/assets/fonts/Outfit-VariableFont.woff2") format("woff2");
  font-weight: 100 900;
  font-display: swap;
}
```

Then, I added a modern and minimal CSS reset:

```css
*,
*::before,
*::after {
  box-sizing: border-box;
}

* {
  margin: 0;
  padding: 0;
  font: inherit;
}

img {
  display: block;
  max-width: 100%;
}
```

Lastly, I learned to avoid using fixed heights and widths on containers.
For the component, I used `max-width`, which prevents it from growing larger than the specified size while allowing it to shrink when needed, such as on mobile screens. To center it, I set the body to `min-height: 100vh;`, since by default the body is only as tall as its content, and then used Flexbox properties. Using `min-height` instead of a fixed `height` ensures the page is at least as tall as the viewport and prevents content from being cut off on smaller screens.
