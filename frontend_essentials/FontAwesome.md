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
1. When you want to use icon in your file, first import `{FontAwesomeIcon}`
```
import { FontAwesomeIcon } from '@fortawesome/react-fontawesome';
```
2. Now, you can import icon as camelCase letter like `{faName}` in your files.  
For example, I'll show how to import [spinner](https://fontawesome.com/icons/spinner?f=classic&s=solid) icon.
```
import { faSpinner } from '@fortawesome/free-solid-svg-icons';
```
Then, call it in your file
```
<FontAwesomeIcon icon={faSpinner} />
```
You can also add style and animation altogether.
```
<FontAwesomeIcon icon={faSpinner} spinPulse style={{color: "#63E6BE",}} />
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
<i className="fa-solid fa-spinner"></i>
```
However, Global import or Html import alone won't work when styles and animations are added.
```
<FontAwesomeIcon icon="fa-solid fa-spinner" spinPulse style={{color: "#63E6BE",}} />
<i class="fa-solid fa-spinner fa-spin-pulse" style="color: #63E6BE;"></i>
```
You must write it in this format.
1. Instead of `FontAwesomeIcon icon`, change into `i className`
2. `spinPulse` won't work, adding `fa-spin-pulse` in className will work.
3. `style={{color: "#63E6BE",}} ` will work. `style="color: #63E6BE;"` not work.
```
<i className="fa-solid fa-spinner fa-spin-pulse" style={{color: "#63E6BE",}}></i>
```
### Error Encounter
```
npm cache clean --force
npm install
```
