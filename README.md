# w3scss 
#npm #node #sass #scss

Rewrite of [W3.CSS](https://www.w3schools.com/w3css/default.asp) in [SCSS](https://sass-lang.com/) with some minor changes and editions. 

I use this as a light and free framework for my other web projects.

---

## Content

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Prerequisities](#prerequisities)
- [Installation](#installation)
- [Usage](#usage)
- [Filestructure](#filestructure)
- [Configuration](#configuration)
- [License](#license)

---
## Features

- Complete Rewrite in [SCSS](https://sass-lang.com/)
- Almost all fixed values from the originial [W3.CSS](https://www.w3schools.com/w3css/default.asp) are configurable via variables
- Compilates to CSS with simple [NPM](https://www.npmjs.com/)-Scripts
- Added some editions from my usage for more comfort (extra margin/padding-classes, animations and effects...)

---

## Tech Stack

- **Frontend:** [SCSS](https://sass-lang.com/)/CSS
- **Backend:** [Node.js](https://nodejs.org/)/[NPM](https://www.npmjs.com)

---

## Voraussetzungen

- [Node.js](https://nodejs.org/) with following packages installed (will be installed with ``npm install`` anyway)
	- [autoprefixer](https://www.npmjs.com/package/autoprefixer) - add vendor prefixes
	- [cssnano](https://www.npmjs.com/package/cssnano) - minimize the file for production
	- [postcss-cli](https://www.npmjs.com/package/postcss-cli) - CLI for [PostCSS](https://www.npmjs.com/package/postcss)
	- [postcss-scss]() - let [PostCSS](https://www.npmjs.com/package/postcss) parse .scss-files
	- [sass](https://www.npmjs.com/package/sass) - well obviously...
	- [stylelint](https://www.npmjs.com/package/stylelint) - linter

---

## Installation

```bash
# clone repository
git clone https://github.com/TeaRexing/w3scss
cd w3scss

# install dependencies
npm install
```

---

## Usage

```js
// build dev version (output won't be minified)
npm run build

// build production version (minified output with vendor prefixes)
npm run production

// or just use the main.css as it is
<link rel="stylesheet" type="text/css" href="main.css">
```

---

## Filestructure

```
projektname/
├── src/
│   ├── index.html
│   ├── style.css
│   └── main.js
├── public/
├── .gitignore
├── package.json
└── README.md
```

---

## Configuration

```scss
// change configuration variables in the main.scss file
$prefix: w3 !default; // follows the original w3.css syntax - change it to your liking
$base-spacing: 8px !default; // default spacing for margins, paddings, etc... changing this will effect almost all containers
$base-font: Verdana !default; // font for everything except headings and code
$heading-font: Segoe UI !default; // font for headings
$code-font: Consolas !default; // font for the code/codespan elements
$content-width: 980px !default; // max-width of the fixed size and centered container
$auto-width: 1140px !default; // max-width of the responsive and centered container
$color-palette: (
  #f15a24, // always the branding color - suffix -1
  #4d4d4d, // always contrast to the branding color - suffix -2
  #000, // suffix -3
  #000, // suffix -4
  #000, // suffix -5
  #000, // suffix -6
) !default;
// for example: .prefix-text-1 will be rendered as
.prefix-text-1 {
	color: #f15a24;
}
// can be used for background, text, hover and borders

/* Breakpoints
 - fix these to your liking
 - this will influence the responsive behaviour of containers
*/
// mobile: smaller equal 600px
$mobile: 600px;
// phablet: between 601px and 768px
$phablet: 768px;
// tablet: between 601px/768px and 992px
$tablet: 992px;
// desktop: larger than 1205px
$desktop: 1205px;

```

---
## License

[MIT](https://rem.mit-license.org/)
