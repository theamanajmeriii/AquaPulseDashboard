Tailwind CSS Practice Project 

This project was created to learn and practice Tailwind CSS using the CLI setup with Vite.

We built:
Tailwind environment setup
Dashboard UI practice
Responsive layouts
Grid & Flexbox concepts
Modern UI styling

![Image Alt](https://github.com/theamanajmeriii/AquaPulseDashboard/blob/5fe0ee47a5301716b6ce87a9eb2715c9f518b4be/AquaDashboard/Screenshot%202026-05-24%20142200.png)
![Image Alt](https://github.com/theamanajmeriii/AquaPulseDashboard/blob/5636d320aff74b86c1423c4b4dd257f3d53e9220/AquaDashboard/Screenshot%202026-05-24%20142442.png)
# Environment Setup

### 1. Initialize npm

Run:

npm init -y

This creates:

package.json

which manages project dependencies and scripts.

---

### 2. Install Vite

Run:

npm install vite

Vite is used for:

* Fast development server
* Hot reload
* Modern frontend workflow
* Optimized build process

---

### 3. Install Tailwind CSS

Run:

npm install -D tailwindcss postcss autoprefixer

These packages are required for Tailwind CSS setup.

---

### 4. Generate Configuration Files

Run:

npx tailwindcss init -p

This creates:

* tailwind.config.js
* postcss.config.js

---

### 5. Configure Tailwind Content

Open:

tailwind.config.js

Add:

/** @type {import('tailwindcss').Config} */
module.exports = {
content: ["./**/*.{html,js}"],
theme: {
extend: {},
},
plugins: [],
}

This tells Tailwind to scan:

* HTML files
* JavaScript files

for utility classes.

---

### 6. Create Tailwind Input CSS

Create:

style.css

Add:

@tailwind base;
@tailwind components;
@tailwind utilities;

These directives load Tailwind's base styles, components, and utility classes.

---

### 7. Build Tailwind Output CSS

Run:

npx tailwindcss -i ./style.css -o ./output.css --watch

Explanation:

* -i → input file
* style.css → Tailwind source file
* -o → output file
* output.css → generated CSS
* --watch → automatically rebuilds on changes

---

### 8. Link CSS with HTML

Inside the HTML <head> tag add:

<link rel="stylesheet" href="output.css">

This loads the generated Tailwind CSS.

---

### 9. Add Vite Script

Inside package.json add:

"scripts": {
"dev": "vite"
}

This creates a shortcut command for starting the Vite development server.

---

### 10. Start Development Server

Run:

npm run dev

Vite will start a local development server and provide a URL such as:

http://localhost:5173

Open it in the browser to view the project.
