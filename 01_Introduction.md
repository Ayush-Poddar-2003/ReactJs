# <CENTER>INTRODUCTION

**WHAT IS REACT ?**  
Open source Js **library** for building UI,  
Developed by Facebook SDE **Jordan Walke** (2013), Got Open Sourced in 2015.   

React Native - for Mobile Apps

---
**HOW IT WORKS?**  
Creates virtual DOM  
Only changes what needs to be changed as previously, DOM used to refresh the whole webpage

---
Essentials -
- NodeJs LTS (Long term support)
- Vite  
Recommended in Offical documentation  
Super fast dev server & Build tool
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

Your project should now run on **localhost : 5173** (Vite’s default port).

---

### <center> WorkFlow
1. index.html is loaded  
`<div id="root"></div>` Everything displayed inside this div   
`<script type="module" src="/src/main.jsx"></script>` To  link  main.jsx
2. main.jsx   
    ```jsx
    createRoot(document.getElementById('root')).render(
    <StrictMode>
        <App /> //App waala main me, main waala root me
    </StrictMode>,
    )
    ```
3. App.jsx and other compments(.jsx) which are linked in main


---
### <CENTER>Updating Project to Latest Version
RC - Release Candidate : Almost ready for final release  

**TO CHECK CURRENT VERSION**
1. Open Project Folder
2. Open Package.json
3. Check Dependancies

**TO UPGRADE**  
1. Open root folder in terminal
2. Run `npm install react@rc react-dom@rc` 