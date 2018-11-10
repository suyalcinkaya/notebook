# Tailwindcss

## React

#### Install dependencies
```js
npm install --save-dev tailwindcss autoprefixer postcss-cli
```

#### Init tailwind config
```js
./node_modules/.bin/tailwind init tailwind.config.js
```

#### Create file called `postcss.config.js` with the following:
```
const tailwindcss = require('tailwindcss');
module.exports = {
  plugins: [
    tailwindcss('./tailwind.config.js'),
    require('autoprefixer'),
  ],
};
```

#### Create `src/styles/index.css` and paste in the following:
```css
@tailwind preflight;
@tailwind utilities;

/* Your custom CSS here */
```

#### Edit package.json file as;
```json
"scripts": {
  "build:css": "postcss src/styles/index.css -o src/index.css",
  "watch:css": "postcss src/styles/index.css -o src/index.css -w",
  "start": "npm run watch:css & react-scripts start",
  "build": "npm run build:css && react-scripts build",
  ...
}
```

#### Import the output css in src/index.js:
```js
import 'index.css';
```
