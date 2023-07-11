# Vanilla JS Filterable List

This repository contains the implementation of a filterable list using vanilla JavaScript. With this project, you can learn how to create a dynamic list that filters and displays items based on user input.

## Features

- Dynamically filter and display list items
- Improve user experience with real-time filtering
- Customizable for your own projects

## Getting Started

1. Clone the repository: `git clone https://github.com/username/vanilla-js-filterable-list.git`
2. Open `index.html` in your preferred web browser.
3. Start filtering the list by typing in the input field.

## Code Example

```javascript

      //selector
      let filterInput = document.querySelector(".filter-input");
      //Add event listener to input field
      filterInput.addEventListener("keyup", filterNames);

      //Filter the list based on user input
      function filterNames() {
        let filterValue = filterInput.value.toUpperCase();
        //get ul
        let ul = document.querySelector(".collections");
        //get lis
        let li = document.querySelectorAll("li.collection-item");

        //create a for loop
        for (let i = 0; i < li.length; i++) {
          let a = li[i].getElementsByTagName("a")[0];
          //if matched
          if (a.innerHTML.toUpperCase().indexOf(filterValue) > -1) {
            li[i].style.display = "";
          } else {
            li[i].style.display = "none";
          }
        }
      }

 
```

## Contributing

Contributions are welcome! If you have any suggestions or improvements, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
