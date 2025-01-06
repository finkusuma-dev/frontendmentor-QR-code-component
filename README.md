# Frontend Mentor - QR code component solution

This is a solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Frontend Mentor - QR code component solution](#frontend-mentor---qr-code-component-solution)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [Screenshot](#screenshot)
    - [Links](#links)
  - [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
      - [Setup The Image Container](#setup-the-image-container)
      - [Drop Shadow](#drop-shadow)
    - [Continued development](#continued-development)
    - [Useful resources](#useful-resources)
  - [Author](#author)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### Screenshot

<img src="./screenshot.jpg" width="400">
<!-- ![<img src="./screenshot.jpg" width="100">](./screenshot.jpg) -->

### Links

- Solution URL: [https://github.com/finkusuma-dev/frontendmentor-QR-code-component](https://github.com/finkusuma-dev/frontendmentor-QR-code-component)
- Live Site URL: [https://finkusuma-dev.github.io/frontendmentor-QR-code-component](https://finkusuma-dev.github.io/frontendmentor-QR-code-component)

## My process

### Built with

- Semantic HTML5 markup
- CSS
- Flexbox

### What I learned

#### Setup The Image Container

I learned how to make a lazy loading image, and to properly setup the image container dimensions:

```html
<img
  src=" ./images/image-qr-code.png"
  alt="QR code"
  loading="lazy"
  width="576"
  height="576"
/>
```

```css
img {
  width: 100%;
  height: auto;
}
```

When images are lazily loaded, at first the container (**img** element) height is zero. Then when the images are successfully downloaded and shown on the page, the images suddenly appear and makes what was on the page jump. This can happen when the image is on top of the page, and really annoying when you're just start reading or clicking on a button. I still encountered this on some of the pages on the web.

To solve this jump problem, I set the `width` and `height` of **img** to the actual dimensions of the image (or you can set it to other values as long as they have the same aspect ratio to the actual image dimensions). Then, on CSS I set the `width` to be **100%** and set the `height` to **auto**. This will make the browser calculate the height of the img element using the `width` and `height` attributes as a ratio against the width of the **img** element itself (which I already set it to 100% of the parent container).

This way, the image container will have the correct height of the image that is still being downloaded and the ugly jump won't happen.

#### Drop Shadow

I wanted to put shadow on the card just like on the project preview image, but looked on the figma style I couldn't find the detailed values of the drop shadow being used. So I just tried with different values and found this similar with the design:

```css
.card {
  box-shadow: 0px 15px 20px 0px hsl(0, 0%, 0%, 0.05);
}
```

### Continued development

Currently I've tried to apply the semantic HTML, but I don't know if my code is correct or not. If anyone has suggestions of how to improve it, please contact me via Twitter, or you can also open a GitHub issue.

And please if anyone know the exact value of the drop shadow used in figma, I need it for the future project. Thanks in advance.

### Useful resources

- [Cumulative Layout Shift](https://web.dev/learn/images/performance-issues?authuser=1#cumulative_layout_shift) - This is the learning resource that I used to prevent the jump problem by properly setup the **img** element.

## Author

- Github - [Arifin Kusuma](https://github.com/finkusuma-dev)
- Frontend Mentor - [@finkusuma-dev](https://www.frontendmentor.io/profile/finkusuma-dev)
- Twitter - [@finkusuma_dev](https://www.twitter.com/finkusuma_dev)
