# az-resume
Developing skills on Azure by following [guided project](https://www.youtube.com/watch?v=ieYrBWmkfno).

## First Steps
- Updated the structure and added main.js file
- main.js files holds the code for the counter on the home page which counts the visitors on the page.
```js
window.addEventListener('DOMContentLoaded', (event) =>{
    getVisitCount();
})


const functionAPI = '';

const getVisitCount = () => {

    let count = 30;
    fetch(functionAPI).then(response => {
        return response.json()
    }).then(response =>{
        console.log("Website called Function API.");
        count = response.count;
        document.getElementById("counter").innerText = count;
    }).catch(function(error){
        console.log(error);
    });
    return count;
}
```
- We have to provide the function URL after creating it in Azure