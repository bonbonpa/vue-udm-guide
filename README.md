> start : 2017-05-22

## dvp-NotN : Vue.js the complete guide from udemy

### Sec 1-2 : Let's Create our First VueJS Application

[vuejs.org](https://vuejs.org/v2/guide/)

> go jsfiddle

#[demo](https://jsfiddle.net/bonbonpa/t8xw7guv/)

```html
<script src="https://unpkg.com/vue/dist/vue"></script>
<div id="app">
  <p>{{title}}</p>  
</div>

<script type="text/javascript">
new Vue({
  el: '#app',
  data: {
  title: 'Hello bonbonpa'
  }
});
</script>
```
### sec 1-3 Extending the VueJS Application

```html
<script src="https://unpkg.com/vue/dist/vue"></script>

<div id="app">
  <input type="text" v-on:input="changeTitle">
  <p>{{title}}</p>  
</div>

<script type="text/javascript">
new Vue({
  el: '#app',
  data: {
  title: 'Hello bonbonpa'
  },
  methods: {
    changeTitle:  function(event){
      this.title = event.target.value;
      // access to data
    }
  }
});
</script>
```
[demo](https://jsfiddle.net/bonbonpa/kubpwt9h/)

### sec 1-4 Course Structure

About this Course

- Gettting Started
- Interacting with the DOM(template)
- Understandibf the VueJS Instance
- Vue CLI
- Components
- Forms
- Directives, Filter & Mixins
- Animations & Transitions
- Working with Http
- Routing
- State Management
- Deploying a VueJS App

### sec 1-5 Take Advantage of all Course Resources!

Projects, Exercises, Code and Questions

- 1st Project : Basics, Template Interaction
- 2nd Project : Components
- 3rd Project : Animations
- 4th Project : Final Project (incl. Routing,State Management)
