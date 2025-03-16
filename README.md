Neodom is a small javascript library that allows you to modify, alter and style an HTML element using a small line of code instead of class names.

- It has its own simple expression evaluator
- Transform elements using custom functions
- Easy to implement

> [!NOTE]
> Development is in its early stages!

```javascript
neodom_init(); //init singleton State

//register functions
neodom_func(State.Singleon, 'rand_number', 0, () => {
    return Math.floor(Math.random() * 100);
});
neodom_func(State.Singleton, 'set', 1, (value) => {
  State.Singleton.dom.innerText = value;
});
neodom_start(State.Singleton); //start neodom

```
> [!WARNING]
> Always start with the 'neo' tag before writing your expression!
```html
<p class="neo set(rand_number())">This text will be replaced with a random value</p>
```
