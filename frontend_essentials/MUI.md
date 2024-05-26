## Material UI
[Installation Docs](https://mui.com/material-ui/getting-started/installation/)

```
npm install @mui/material @emotion/react @emotion/styled
```
For icons
```
npm install @mui/icons-material
```
Material UI uses the Roboto font by default. Add it to your project via Fontsource, or with the Google Fonts CDN.
```
npm install @fontsource/roboto
```
Then you can import it in your entry point like this:
```
import '@fontsource/roboto/300.css';
import '@fontsource/roboto/400.css';
import '@fontsource/roboto/500.css';
import '@fontsource/roboto/700.css';
```
> Fontsource can be configured to load specific subsets, weights and styles. Material UI's default typography configuration relies only on the 300, 400, 500, and 700 font weights.

To install Roboto through the Google Web Fonts CDN, add the following code inside your project's <head /> tag:
```
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link
  rel="stylesheet"
  href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap"
/>
```
To install the Material Icons font in your project using the Google Web Fonts CDN, add the following code snippet inside your project's `<head />` tag:
> To use the font Icon component, you must first add the [Material Icons](https://fonts.google.com/icons?icon.set=Material+Icons) font. Here are some [instructions](https://mui.com/material-ui/icons/#icon-font-icons) on how to do so. For instance, via Google Web Fonts:
```
<link
  rel="stylesheet"
  href="https://fonts.googleapis.com/icon?family=Material+Icons"
/>
```
### Error Encounter
Please note that react and react-dom are peer dependencies, meaning you should ensure they are installed before installing Material UI.
```
"peerDependencies": {
  "react": "^17.0.0 || ^18.0.0",
  "react-dom": "^17.0.0 || ^18.0.0"
},
```
