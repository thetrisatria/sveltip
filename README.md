# Sveltip

Simple tooltip component for [Svelte](https://svelte.dev), comes with light and dark theme.

## Get started

### Installation
```sh
npm install sveltip
```

### Usage
First you need to import it on the script section
```js
// ...
	import Sveltip from 'sveltip';
// ...
```
and then use it on your application. Here's some example code:
```html
    <Sveltip top dark text="Click me to begin">
        <button>Start</button>
    </Sveltip>

    <Sveltip bottom light text="Click me to begin">
        <button>Start</button>
    </Sveltip>

    <Sveltip right dark text="Dolor Sit Amet">
        <h1>Lorem Ipsum</h1>
    </Sveltip>
```

### Properties
These are all available props, please refer the sample above on how they work
```js 
text 
// Text displayed on the tooltip
```
```js
light
// Light mode for the tooltip bubble
```
```js
dark
// Dark mode for the tooltip bubble
```
```js
top
// Put the tooltip on the top of element
```
```js
bottom
// Put the tooltip on the bottom of element
```
```js
left
// Put the tooltip on the left side of element
```
```js
right
// Put the tooltip on the left side of element
```