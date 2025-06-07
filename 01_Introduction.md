# <CENTER>INTRODUCTION

**WHAT IS REACT ?**  
Open source Js library for building UI,  
Developed by Facebook SDE Jordan Walke (2013), Got Open Sourced in 2015.   
We make Single Page Application  
React Native for Mobile Apps

---
**HOW IT WORKS?**  
Creates virtual DOM  
Only changes what needs to be changed as previously  
DOM used to refresh the whole webpage

---
Essentials -
- NodeJs
- Vite  
Recommended in Offical documentation  
Super fast dev server
- bun instead of npm as 29x faster

---
### Our First React App

   Go to https://vite.dev/guide/ for steps
1. Open cmd and go to folder.
2. `npm create vite@latest`
3. Will ask to name project, Select framework - choose react, variant - select Javascript
4. `cd ProjectName` 
5. `npm install`  
All above steps will add needed files for the App.
6. `npm run dev`

Your project should now run on localhost:5173 (Vite’s default port).

---

### <center> WorkFlow
1. index.html is loaded  
`<div id="root"></div>` Everything inside this div   
`<script type="module" src="/src/main.jsx"></script>`
2. main.jsx   
    ```jsx
    createRoot(document.getElementById('root')).render(
    <StrictMode>
        <App /> //App waala main me, main waala root me
    </StrictMode>,
    )
    ```