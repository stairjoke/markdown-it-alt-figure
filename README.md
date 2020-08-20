# Markdown It Figure

[Markdown-It](https://markdown-it.github.io/) plugin that allows you to add [`<figure>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/figure)s with [`<figcaption>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/figcaption)s to your Markdown.

## Install

```bash
npm install @rbottomley/markdown-it-figure
```

## Usage

### Markdown-It Config

```js
const markdown = require('@rbottomley/markdown-it');

const md = markdown({
  /* ... markdown-it options */
}).use(require('@rbottomley/markdown-it-figure'));
```

### Basic figure

#### Markdown
```md
#[Caption](/url/to/image.png)
```

#### Generated HTML
```html
<figure>
  <img src="/url/to/image.png" />
  <figcaption>Caption</figcaption>
</figure>
```

### Advanced figure

Includes a figure number and alt text for image.

#### Markdown
```md
#1234[Caption](/url/to/image.png [Alt Text])
```

#### Generated HTML
```html
<figure id="figure-1234">
  <img src="/images/foo.png" alt="Alt Text" />
  <figcaption>
      <span class="figure-id">1234: </span>
      Caption
  </figcaption>
</figure>
```

## Changelog

### 1.0.1
- update dependencies.

### 1.0.0
- remove P tag from FIGCAPTION output.

### 0.2.0
- fork from @chromeos/static-site-scaffold-modules.

