template: [astro-theme-cuctus](https://github.com/chrismwilliams/astro-theme-cactus)

> Technologies
> 
> Astro: Build fast websites, faster.
> 
> Tailwind CSS: Rapidly build modern websites without ever leaving your HTML.
> 
> Markdown: Simple and easy-to-use markup language.
> 
> MDX: Markdown for the component era.
> 
> Satori: Generating png Open Graph images for blog posts.
> 
> Pagefind: A fully static search library.
> 
> Astro Icon: An easy to use Icon component for Astro.
> 
> Expressive Code: Highly customisable source code & syntax highlighter

## Set default LightMode/DarkMode

src/utils/domElements.ts

```ts
export function rootInDarkMode() {
	return document.documentElement.getAttribute("data-theme") === "dark";
}
```

### lazy load

```html
<img src="image.jpg" loading="lazy" alt="portfolio image" />
```

- plugin

```
npm install @astrojs/image
```

```js
// astro.config.mjs
import { defineConfig } from "astro/config";
import image from "@astrojs/image";

export default defineConfig({
	integrations: [image()],
});
```

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## 👀 Want to learn more?

Feel free to check [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).
