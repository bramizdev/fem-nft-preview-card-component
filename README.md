# Frontend Mentor - NFT preview card component solution

This is my solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

- Desktop
![Captura de pantalla 2023-02-15 a las 18 53 38](https://user-images.githubusercontent.com/112894363/219230740-ecd9ea96-3fc9-447f-b4b3-043b544ef540.png)

- Mobile
![Captura de pantalla 2023-02-15 a las 18 53 46](https://user-images.githubusercontent.com/112894363/219230805-65624281-378d-46ad-a700-8198e943f8ed.png)

### Links

- Solution URL: [https://github.com/bramizdev/fem-nft-preview-card-component](https://github.com/bramizdev/fem-nft-preview-card-component)
- Live Site URL: [https://bramizdev.github.io/fem-nft-preview-card-component/](https://bramizdev.github.io/fem-nft-preview-card-component/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

I didn't know how to create an overlay to an image, this is the aproach that I took.

Since this was a link I used a ```<a>``` tag as a container, because I thought when you click at the image it will take you to another page with more details of this NFT.

```html
  <a href="#" class="card__url-container">
    <img
      src="./images/image-equilibrium.jpg"
      alt="A transparent cube balanced in one of its corners in a dark blue background promoting balance and calm"
      width="604"
      height="604"
      class="card__img"
    />
    <div class="overlay">
      <img src="./images/icon-view.svg" alt="" aria-hidden="true" />
    </div>
  </a>
```

```css
.card__img {
  border-radius: 0.5rem;
}

.card__url-container {
  position: relative;
}

.overlay {
  position: absolute;
  background-color: var(--clr-primary-500);
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  height: 100%;
  width: 100%;
  display: grid;
  place-items: center;
  border-radius: 0.5rem;
  opacity: 0;
  transition: 0.4s ease;
}

.card__url-container:hover .overlay {
  opacity: 1;
  background-color: var(--clr-primary-500-op);
}
```

## Author

- Website - [@brymizdev](https://github.com/bramizdev)
- Frontend Mentor - [@brymizdev](https://www.frontendmentor.io/profile/bramizdev)
