# azure-resume

My own azure resume,, following [ACG project video.](https://www.youtube.com/watch?v=ieYrBWmkfno)

## First steps

- Frontend folder contains the website.

- main.js contains visitor counter code.

```js
window.addEventListener("DOMContentLoaded", (event) => {
  getVisitCount();
});

const functionApi = "";

const getVisitCount = () => {
  let count = 30;
  fetch(functionApi)
    .then((response) => {
      return response.json();
    })
    .then((response) => {
      console.log("Website called function API.");
      count = response.count;
      document.getElementById("counter").innerText = count;
    })
    .catch(function (error) {
      console.log(error);
    });
  return count;
};
```
