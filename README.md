# HackPrac
## Font Awesome
[Installation Docs](https://docs.fontawesome.com/web/use-with/react/)
### First install fontawesome
```
npm i --save @fortawesome/fontawesome-svg-core
```

### Then, icons
```
npm i --save @fortawesome/free-solid-svg-icons
npm i --save @fortawesome/free-regular-svg-icons
npm i --save @fortawesome/free-brands-svg-icons
```
#### Individual Import
When you want to use icon in your file, first import `{FontAwesomeIcon}`
```
import { FontAwesomeIcon } from '@fortawesome/react-fontawesome';
```
You can import icon as camelCase letter with {faName} in your files.  
For example, I'll show how to import [map-location-dot](https://fontawesome.com/icons/map-location-dot?f=classic&s=solid) icon.
```
import { faMapLocationDot } from '@fortawesome/free-solid-svg-icons';
```
Then, call it in your file
```
<FontAwesomeIcon icon={faMapLocationDot} />
```
#### Global Import
If you don't want to import individual icon each time, you can globally import only once.
```
npm install --save @fortawesome/fontawesome-free
```
In `main.jsx`, add this line
```
import '@fortawesome/fontawesome-free/css/all.css';
```
You can now add your favorable icons in your files in this tag format.
```
<i className="fa-solid fa-map-location-dot"></i>
```
## Tailwind
[Installation Doc](https://tailwindcss.com/docs/guides/vite)

Install tailwindcss and its peer dependencies, then generate your `tailwind.config.js` and `postcss.config.js` files.
```
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```
Add the paths to all of your template files in your `tailwind.config.js` file.
```
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
Add the @tailwind directives for each of Tailwind’s layers to your `./src/index.css` file.
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

## React Router DOM
```
npm install react-router-dom
```
```
import React from 'react'
import ReactDOM from 'react-dom/client'
import { createBrowserRouter, RouterProvider} from "react-router-dom";
import App from './App.jsx'
import './index.css'

const router = createBrowserRouter([
  {
    path: "/",
    element: <App/>,
  },
]);

ReactDOM.createRoot(document.getElementById("root")).render(
  <React.StrictMode>
    <RouterProvider router={router} />
  </React.StrictMode>
);

```
#### Outlet
- Purpose: <Outlet /> is used to render nested route components within a parent component.
- Usage: Place <Outlet /> in the parent route's component where you want the child route components to be rendered.
- Effect: When a child route is matched, its component replaces the <Outlet /> in the parent component.
```
import { Outlet } from "react-router-dom";
<Outlet />
```
In `main.jsx`
```
{
    path: "/contact",
    element: <ContactPage/>,
    children:[
      {
        path: "phone",
        element: <PhoneBox/>,
      },
      {
        path: "phone",
        element: <ProfileBox/>,
      },
    ]
  },
```

#### useNavigate
```
import { useNavigate } from 'react-router-dom';

const navigate = useNavigate();
navigate('/another-page');
```
#### useParams
```
import {useParams} from 'react-router-dom';

const { id } = useParams();
```
#### useSearchParams
```
import { useSearchParams } from 'react-router-dom';

const [searchParams] = useSearchParams();
const queryId = searchParams.get('id');
```
#### useLocation

useLocation will return information of current URL such as :
pathname  path of current URL
search query parameters in current URL ex. "?id=123&name=John".
hash hash fragment in URLe ex."#section-2".
state state datanavigate from another page.
```
import { useLocation } from "react-router-dom";

const location = useLocation();
//location.pathname === "/" ? "#2F69D9" : "#eeeeee",

```
## Other Essentials
```
npm install react-responsive-carousel
npm install react-scroll react-icons
```
