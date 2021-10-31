# Learning Svelte (personal repo)

## Notes
Svelte is a lightweight, truly reactive framework for building frontend applications
There exists a framework built on top of Svelte, called Sapper, which is often used for bigger applications in companies

Svelte applications are made up of Svelte-components which is basically mini-HTML pages.
root component is often called app.svelte  
  

Send values to a Svelte component
```
<Age age={age}/>
```
If the variable sent in is the same name as the variable in the Svelte component you're callinh you can simplify it by writing it like this;
```
<Age {age} />
```  
  
  
  

To make a variable reactive declare it using ``` $: dogYears = age * 7; ```
This will change the value of the variable dogYears if age changes