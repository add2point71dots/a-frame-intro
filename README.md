# An Intro to VR & A-Frame
An introduction to VR and building VR experiences with A-Frame

## What is Virtual Reality?
Virtual Reality, or VR, simulates a user’s physical presence in a virtual or imaginary environment

VR is more than just games. There’s VR film and video, documentaries, news stories, journals, adventures, and more.

### Criticisms to VR
- Accessibility to enjoy (equipment, culture)
- Accessibility to develop (isolated)
- Misguided “Empathy Machines”
- Sexual Harassment possibilities

## What is A-Frame?
A web framework for building virtual reality experiences
- is open-source and accessible by web
- has a deep, small community backed by Mozilla
- uses markup that looks like HTML to be placed in .html files
- encourages fast development/prototyping

### Useful Concepts
- Uses 3D coordinate space like (0, 0, 1)
- Assets are 3D shapes (primitives) or 3D models, or more
- Some special effects are made with particle effects

### How does A-Frame work?
- Load in the A-Frame framework as javascript
- Put things in a scene
- Asset manager loads declared assets
- Follows an ["entity-component system"](https://aframe.io/docs/0.5.0/introduction/entity-component-system.html), meaning that an entity (container object) is built from composing together different components (reusable module). In this case, we create HTML entities and define its components as HTML attributes, like so:

```
<a-entity propertyName1="propertyValue1" propertyName2="propertyValue2"></a-entity>
```

# Hello World Tutorial

## Install
1. In the terminal, clone the repo using `git clone https://github.com/dannielle/a-frame-intro.git`
2. Navigate to the project with `cd a-frame-intro`
3. Install the dependencies with `npm install`

## Import
1. Open up `index.html`
2. Find the head tag and use the correct tag to point to the minified A-frame javascript.

## Hello World!
1. Read the docs on [the a-text tag](https://aframe.io/docs/0.5.0/primitives/a-text.html).
2. Within the `a-scene` tag, add an `a-text` tag with a `value` of "Hello World!", a `color` of "#000000" and a `position` of "-1 2 -3"

## Run
1. In your terminal, run the server using `npm start`. Your browser should open up http://localhost:3000/
2. Verify that you see the Hello World text

## Iterate
1. Add a light source to the scene using an `a-light` tag. The `type` is "ambient" and the `color` is "#222".
1. Add a box to the scene using an [`a-box`](https://aframe.io/docs/0.5.0/primitives/a-box.html) tag. The `position` is "0 0.5 -3", the `rotation` is "0 45 0", and the `color` is "#DEFACE".
2. In the assets tag, import the asset using an `img` tag with a `src` of `assets/beltline.jpeg` and an `id` of "sky"
3. Create an [`a-sky`](https://aframe.io/docs/0.5.0/primitives/a-sky.html) tag in the `a-scene` tag but outside of `a-assets`. The value of the sky's source is the `#sky` id that refers to the asset
4. In the assets tag, import the asset using an `a-asset-item` tag with a src `assets/bicycle.dae` and an `id` of "bike"
5. Add an [`a-collada-model`](https://aframe.io/docs/0.5.0/primitives/a-collada-model.html) tag under the sky tag. The value of the model's source is the "#bike" id. The `position` is "3 1 -2" and the `rotation` is "0 90 0".

## Run on Phone
1. Make sure your phone and computer are connected to the same Wifi network.
2. Find your IP Address. On macs, this is found in System Preferences > Network, and under the "Status" heading.
3. On your phone, navigate to `<Your IP address>:3000`

# More Resources
- [The Docs](https://aframe.io/docs/0.5.0/introduction/)
- [Examples (with source code)](https://aframe.io/examples/)
- [Collection of extended A-Frame components](https://github.com/aframevr/awesome-aframe)
