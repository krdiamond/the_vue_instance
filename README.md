# THE VUE INSTANCE

## Creating a Vue INSTANCE
```
var vm = new Vue({
  //options object goes here
})
```
- To create a new Vue application create a new Vue instance using this syntax
- All view components are also Vue instances

## Data Objects
- When a new instance of Vue is created, a data object should be included
- When the data's key is included in the html `{{ example }}` the value will be displayed
- When any of the values in the data object change throughout the code, Vue will re-render the DOM
- This only works if the property was originally declared in the new instance
    - If the property starts out as empty or non-existent it will need a place holder to use later
    ```
    data: {
      newTodoText: '',
      visitCount: 0,
      todos: [],
      error: null
    }
    ```
## Instance Lifecycle
These are the automatic Lifecycle instances:
1. Set up Data Observation
2. Compile template
3. Mount the instance to the DOM
4. Update the Dom when data changes

Hooks can be implemented by choice:
- Created: used to run some code after an instance is created
- Mounted
- Updated
- Destroyed

- Do not use arrow functions, they will be bound to the parent function and not the Vue instances
- Lifecycle hooks are called with their this pointing to the Vue instance invoking it
