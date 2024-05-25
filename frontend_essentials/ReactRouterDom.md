## React Router DOM
```
npm install react-router-dom
```
In `main.jsx`
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