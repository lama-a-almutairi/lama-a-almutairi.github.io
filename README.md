# Lama Almutairi

Source code for my academic website, built with [Astro](https://astro.build) and [Tailwind CSS](https://tailwindcss.com).

## Pages

| Tab      | File                       | Content                                  |
| :------- | :------------------------- | :--------------------------------------- |
| Home     | `src/pages/index.astro`    | Intro, photo and contact links           |
| About    | `src/pages/about.astro`    | Background                               |
| Projects | `src/pages/projects.astro` | Projects, each with an image and summary |
| Teaching | `src/pages/teaching.astro` | Teaching, each with an image and summary |
| CV       | `src/pages/cv.astro`       | CV shown as a PDF, with a download link  |

## Run locally

Requires Node 24 and [pnpm](https://pnpm.io).

```bash
pnpm install
pnpm dev
```

The site runs at `http://localhost:4321`.

| Command        | Action                      |
| :------------- | :-------------------------- |
| `pnpm dev`     | Start the local dev server  |
| `pnpm build`   | Build the site to `./dist/` |
| `pnpm preview` | Preview the build locally   |
| `pnpm check`   | Run type checks and lint    |

## Update the content

- **Projects and teaching:** edit the list at the top of `src/pages/projects.astro` or `src/pages/teaching.astro`. Each entry needs a `title` and `description`, and can also have an `image` and `imageAlt`. Teaching entries can have an `org` and `date` too. Entries without an image show a placeholder.
- **Images:** put them in `public/projects/` or `public/teaching/`, then refer to them as `/projects/my-image.png` or `/teaching/my-image.png`.
- **Home photo:** follow the comment next to the placeholder in `src/pages/index.astro`.
- **CV:** replace `public/Lama_Almutairi_CV.pdf`, keeping the same file name.
- **Contact links:** edit `src/components/SocialList.astro`.
- **Tabs, name and site URL:** edit `src/site.config.ts`.

## Deployment

The build output in `./dist/` is a static site. All internal links start from the site root, so the site must be served from the root of its domain rather than a subfolder. See [Astro's deployment guide](https://docs.astro.build/en/guides/deploy/github/) for GitHub Pages.

## Credits

Built on the [Astro Cactus](https://github.com/chrismwilliams/astro-theme-cactus) theme by Chris Williams, used under the MIT License. See [LICENSE](LICENSE).
