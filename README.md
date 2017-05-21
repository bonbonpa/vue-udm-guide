> start : 2017-05-22

## dvp-NotN : Vue.js the complete guide from udemy

### Let's Create our First VueJS Application

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
