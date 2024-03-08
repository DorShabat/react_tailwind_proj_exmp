# Getting Started with Create React App with Tailwind

in order to initialize react app with tailwind we will do the following:

1. create a new repository
2. open github desktop and clone the new repo to local folder
3. open the local folder in vs code
4. open teminal in vs code 
5. use `npx create-react-app .`
6. use `npm install -D tailwindcss postcss autoprefixer`
7. use `npx tailwindcss init -p`
8. add these lines:
@tailwind base;
@tailwind components;
@tailwind utilities;
to src/index.css
9. use `npm install gh-pages --save-dev`
10. Add the following scripts to your package.json:
* dont forget to Replace <username> with your GitHub username and <repository-name> with the name of your GitHub repository.
```
"scripts": {
  "predeploy": "npm run build",
  "deploy": "gh-pages -d build",
  ...
},
"homepage": "http://<username>.github.io/<repository-name>",
```
11. replace the content in tailwind.config.js to : 
/** @type {import('tailwindcss').Config} */
module.exports = {
  purge: ['./src/**/*.{js,jsx,ts,tsx}', './public/index.html'],
  darkMode: false, // or 'media' or 'class'
  theme: {
    extend: {},
  },
  variants: {
    extend: {},
  },
  plugins: [],
};

12. commit and push using the github desktop
13. use `npm run deploy`
14. now it is in the github pages. 

#in order to view the site local: 
1. use `npm start`

# in order to update the code in github 
1. make the changes you want
2. commit and push 
3. use `npm run deploy`