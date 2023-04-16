# Kirby Plainkit with esbuild

I'm not a big fan of complex build setups. So this is the easiest way to compile JavaScript and Sass[^1] files with live reloading I could come up with. The only files I added to Kirby's plainkit[^2] are a [package.json](package.json) and [assets.config.js](assets/assets.config.js). If you want to use this setup elsewhere, just copy these files to your Kirby project.

![preview](https://user-images.githubusercontent.com/7975568/211556394-2fe0aad2-358b-4a65-a032-b5e2a6548775.gif)

## Features

✨ Bundles and minifies JavaScript with [esbuild](https://esbuild.github.io/).

🎨 Compiles and minifies Sass with [esbuild](https://esbuild.github.io/), [esbuild-sass-plugin](https://github.com/glromeo/esbuild-sass-plugin) and [autoprefixer](https://github.com/postcss/autoprefixer).

⚡ Live reloading with [Browsersync](https://browsersync.io/) for files in `assets/`, `content/` and `site/`.

🐘 Automatically sets the `.test` domain for [Laravel Valet](https://github.com/laravel/valet).

## Setup

Run `npm install` to install the dependencies I defined in the [package.json](package.json). Run `npm run dev` to start the development server.

Have a look at [assets.config.js](assets/assets.config.js) to see how to configure the build process. By default the script compiles `assets/js/main.js` and `assets/scss/style.scss` but you can change this by editing the `jsFiles` and `cssFiles` variables.

I tried to keep it as simple as possible and commented the file as good as I could. If you have any questions, feel free to open an issue.

[^1]: I tried switching to PostCSS and native CSS nesting but I didn't like it. For now I'll stick with Sass.
[^2]: Please refer to Kirby's [Plainkit repository](https://github.com/getkirby/plainkit) for more information about Kirby and their license.