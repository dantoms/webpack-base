# webpack-base
A simple webpack config


## Setup

Run these commands in the terminal

```bash
npm init -y --init-type=module
npm install --save-dev webpack webpack-cli
```

## Handle HTML
```bash
npm install --save-dev html-webpack-plugin
```
The default location is `./src/template.html`

## Handle CSS
```bash
npm install --save-dev style-loader css-loader
```
> [!IMPORTANT]
> ### Loader order matters for CSS!
> Notice how we put css-loader at the end of the array. We must set this order and not the reverse.
>
> Webpack will run the loaders starting at the end, so we want it to read the CSS file into a string with css-loader first, then use style-loader to inject the JavaScript that applies the CSS in that string to the page. It wouldn’t work the same the other way round.

### Import css in JS file
```bash
import "./styles.css"
```