# Learning Svelte (personal repo)

## Recommended videos
[Vite 2.0 Crash Course [15:35]](https://www.youtube.com/watch?v=LQQ3CR2JTX8)
[Learn the Svelte JavaScript Framework - Full Course [7:10:52]](https://www.youtube.com/watch?v=ujbE0mzX-CU&t=3756s)
[Rich Harris - Rethinking reactivity [36:44]](https://www.youtube.com/watch?v=AdNJ3fydeao)

## Notes
Svelte is a lightweight, truly reactive framework for building frontend applications
~~There exists a framework built on top of Svelte, called Sapper, which is often used for bigger applications in companies~~, Sapper have been replaced with <b>SvelteKit</b>

Svelte applications are made up of Svelte-components which is basically mini-HTML pages.
root component is often called app.svelte  

## SvelteKit
SvelteKit is an application framework powered by Svelte. In comparison to vanilla Svelte or Sapper SvelteKit uses [Vite](https://vitejs.dev/) for bundling instead of Rollup. 
### Vite
During development Vite utilizes HMR (Hot Module Replacement) and demand-file serving over native ESM (ESModules), this means no unnecessary bundling of components which have not been changed. Vite also offers flexible programmatic APIs with full TS-typing (TypeScript) and out-of-the-box support for TypeScript, JSX, CSS, JS and more.
<br><br>
When deploying to production Vite bundles everything together using Rollup with multi-page and library mode support.
<br><br>
One of the major perks of using Vite for frontend development is the simple routing-procedure. Vite is basing it's routing on the folder structure of the project, for example if we want to add a page to our app with the url {root}/stockholm we only need to make sure that the page-component is located inside a sub-folder called <b>stockholm</b>

<br><br>  
### Random notes
Send values to a Svelte component
```
<Age age={age}/>
```
If the variable sent in is the same name as the variable in the Svelte component you're callinh you can simplify it by writing it like this;
```
<Age {age} />
```  
<br><br>
To make a variable reactive declare it using ``` $: dogYears = age * 7; ```
This will change the value of the variable dogYears if age changes