# Frontend Mentor - QR code component solution

This is a solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Screenshot](#screenshot)

## Overview

A solution to the QR code component challenge.

Hello (FE) World! This is the first FEM project that I completed. No routing, threads, cacheing, rpcs ;)

### Links

- Solution URL: [](https://your-solution-url.com)

## My process
- VSCode with LiveView to develop & debug
- git for version control
- stack overflow for technical support

### Built with

- semantic HTML5 markup
- CSS custom properties
- CSS Grid layout styles

### What I learned

I had trouble figuring out how to responsively position the QR card in the center of the viewport, but eventually I figured out how to do this using fixed position and translation:

```css
.container {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    ...
}
```

I also learned about two methods of using custom fonts on a website.

1. Using the ```<link>``` tag in the HTML file allows for alternative style sheets to be loaded. It can also facilitate preloading of fonts to avoid jittering of content as the font resource is loaded in the browser after the text is painted. The properties ```rel="preload"``` and ```rel="prefetch"``` can be used on the ```<link>``` tag to achieve this. 

2. Using ```@import``` in a master CSS file streamlines the html ```<head>``` markup because it only needs to link a single style sheet. However, ```@import``` can incur some delay for styles to be applied when loading a page because it defers the loading of the resource. Some build tools flatten the ```@import```s, which can be brittle if the font provider is dynamic.

Both methods allow for the ```media-type``` attribute, which can be used to hide styles from older browsers.

It is common convention to use ```<link>``` for a master style sheet and ```@import``` other style sheets from the master style. For fonts, ```<link>``` is recommended, and making sure the custom font is hosted on a fast CDN. However this sounds like generic advice for any asset that you to be quickly loaded, or to have custom control over progressing painting as the page loads.

### Continued development

I'd like to use semantic tags further and really learn to optimize the html structure to be as lean as possible while still achieving the desired design outcome.

### Useful resources

- ["Preload, prefetch, and other <link> tags"](https://3perf.com/blog/link-rels/) - One can go down the rabbit-hole of browser asset loading...

- [Atlassian tutorial on .gitignore](https://www.atlassian.com/git/tutorials/saving-changes/gitignore) - This helped  refresh my knowledge of ```.gitignore`` in order to avoid commiting images and other assets to repos.

## Author

- Website - [Dan Cocuzzo](https://www.danc.bike)
- Frontend Mentor - [@cocuzzo](https://www.frontendmentor.io/profile/cocuzzo)

### Screenshot

!["qr-code-screenshot"](./screenshot.png)
