# vite-plugin-html-purgecss
This [Vite](https://github.com/vitejs/vite) plugin purges CSS based on HTML output using [PurgeCSS](https://github.com/FullHuman/purgecss).

✔️ Works with Multi Page App 

✔️ Content/pattern setup is not required - plugin purges styles over the whole HTML code which is being resolved by Vite

✔️ If you need to supply extra content (external HTML files, that is possible as an option)

✔  Classes can be dynamically created (`'bg-' + true ? 'red' : 'blue'`) because PurgeCSS runs over already generated HTML (_post_).

## Install
**Yarn**
```
yarn add vite-plugin-html-purgecss-extended -D
```
or **npm**
```
npm i vite-plugin-html-purgecss-extended --save-dev
```

## Usage
### Configuration
Use plugin in your Vite config (`vite.config.ts`)
```
import htmlPurge from 'vite-plugin-html-purgecss-extended'

export default {
    plugins: [
        htmlPurge(),
    ]
}
```

## Options

| Parameter | Type  | Description |
| ----------- | -----------  | ----------- |
| options | `VitePurgeCSSOptions` | A subset of [UserDefinedOptions defined here in the purgecss docs](https://purgecss.com/configuration.html#options).

`VitePurgeCSSOptions` exposes `"content" | "variables" | "defaultExtractor" | "safelist"`
