> start : 2017-05-22

## dvp-NotN : Vue.js the complete guide from udemy

## Section 1 : Getting Started
### Sec 1-1 : Course Introduction
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
- Understanding the VueJS Instance
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

### sec 1-6 Setup VueJS Locally

```html
<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <title>VueJS sec 1-6</title>
  <link rel="stylesheet" href="">
  <script src="vue.js"></script>
</head>

<body>
  <div id="app">
    <input type="text" v-on:input="changeTitle">  
    <p>{{title}}</p>
  </div>
</body>
<script>  
  new Vue({
    el: '#app',
    data: {
      title: 'Hello bonbonpa'
    },
    methods: {
      changeTitle: function(event) {
        this.title = event.target.value;
        // access to data
      }
    }
  });
</script>

</html>
```

## Section 2 Using VueJS to Interact with the DOM

### 2-1 : Module Introduction

DOM Interaction

### 2-2 Understanding VueJS template

can create <template></template>

### 2-3 How to VueJS Template Syntax and Instance Work Together

```html
<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <title>VueJS sec 2-3</title>
  <link rel="stylesheet" href="">
  <script src="vue.js"></script>
</head>

<body''>''
  <div id="app">
    <input type="text" v-on:input="changeTitle">
    <p>{{ sayHello() }}</p> <!--
      exec function
      call function in bracket
    -->
  </div>
</body>[]
<script>
  new Vue({
    el: '#app',
    data: {
      title: 'Hello bonbonpa'
    },
    methods: {
      sayHello: function(event) {
        return 'Hello !';
      }
    }
  });
</script>

</html>
```

### sec 2-4 Accessing Data in the Vue Instance

```html
<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8">
    <title>VueJS sec 2-4</title>
    <link rel="stylesheet" href="">
    <script src="../vue/vue.js"></script>
</head>

<body>
    <div id="app">
        <input type="text" v-on:input="changeTitle">
        <p>{{ sayHello() }}</ p>
        <!--
      exec function
      call function in bracket    7
    -->1
    </div>
</body>
  <script>                    
    ne  w Vue({
        el: '#app',
        data: {
            title: 'Hello bonbonpa'
        },
        methods: {
            sayHello: function() {
                return this.title; // access to properties
            }
        }
    });
</script>

</html>
```

### sec 2-5 Binding to Attributes

```html
<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8">
    <title>VueJS sec 2-5</title>
    <link rel="stylesheet" href="">
    <script src="../vue/vue.js"></script>
</head>

<body>
    <div id="app">
        <input type="text" v-on:input="changeTitle">
        <p>{{ sayHello() }} - <a v-bind:href="link">Google</a></p>
        <!-- con't use {{}} in atrributes' -->
        <!--
      exec function
      call function in bracket
    -->
    </div>
</body>
<script>
    new Vue({
        el: '#app',
        data: {
            title: 'Hello bonbonpa',
            link: 'http://google.com'
        },
        methods: {
            sayHello: function() {
                return this.title; // access to properties
            }
        }
    });
</script>

</html>
```

### Sec 2-6 Understanding and Using Directives

...

### Sec 2-7 Disable Re-Rendering with v-once

```html
<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8">
    <title>VueJS sec 2-7 : Disable Re-Rendering with v-once
    </title>
    <link rel="stylesheet" href="">
    <script src="../vue/vue.js"></script>
</head>

<body>
    <div id="app">
        <h1 v-once>{{ title }}</h1>
        <!-- 2-7: v-once update with 1 time -->
        <p>{{ sayHello() }} - <a v-bind:href="link">Google</a></p>
        <!-- con't use {{}} in atrributes'
         v-bind something you wan bind
         -->
        <!--
      exec function
      call function in bracket
    -->
    </div>
</body>
<script>
    new Vue({
        el: '#app',
        data: {
            title: 'Hello bonbonpa',
            link: 'http://google.com'
        },
        methods: {
            sayHello: function() {
                    this.title = "Hey bonbonpa dvp";
                    return this.title; // access to properties
                }
                //2-7: Keep in mind : All usages of "title" get re-rendered once the property changes!
        }
    });
</script>

</html>
```

### 2-8 How to Output Raw HTML

```html
<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8">
    <title>VueJS sec 2-8 : How to Output Raw HTML
    </title>
    <link rel="stylesheet" href="">
    <script src="../vue/vue.js"></script>
</head>

<body>
    <div id="app">
        <h1 v-once>{{ title }}</h1>
        <!-- 2-7: v-once update with 1 time -->
        <p>{{ sayHello() }} - <a v-bind:href="link">Google</a></p>
        <!-- con't use {{}} in atrributes'
         v-bind something you wan bind
         -->
        <p v-html="finishedLink"></p>
        <!-- 2-8: can't run html for purpose XXS  -->
        <!--
      exec function
      call function in bracket
    -->
    </div>
</body>
<script>
    new Vue({
        el: '#app',
        data: {
            title: 'Hello bonbonpa',
            link: 'http://google.com',
            finishedLink: '<a href="http://google.com">Google</a>'
        },
        methods: {
            sayHello: function() {
                    this.title = "Hey bonbonpa dvp";
                    return this.title; // access to properties
                }
                //2-7: Keep in mind : All usages of "title" get re-rendered once the property changes!
        }
    });
</script>

</html>
```

### Exercise 1

[demo jsfiddle](https://jsfiddle.net/bonbonpa/jLyjaygf/)

### Sec 2-9 Listening to Events

```html
<script src="https://unpkg.com/vue/dist/vue.js"></script>

<div id="app">
  <button v-on:click="increase">Click me</button>
  <p>{{ counter }}</p>
</div>
<script>
new Vue({
	el: '#app',
  data: {
  	counter: 0
  },
  methods: {
  	increase: function(){
    	this.counter++;
    }
  }
});
</script>
```

## [demo](https://jsfiddle.net/7b59gqdz/1/)

### Sec 2-10 Getting Event Data from the Event Object

### Sec 2-11 Passing your own Arguments with Events

### Sec 2-12 Modifying an Event -w ith Event Modifiers

### Sec 2-13 Listening to Keyboard Events

### Exercise 2 Time to Practice - Events

### Sec 2-14 Writing JavaScript Code in the Template

### Sec 2-15 Using Two-Way-Binding

### Sec 2-16 Reacting to Changes with Computed Properties

### Sec 2-17 An Alternative to Computed PropertiesL Watching for Changes

### Sec 2-18 Saving Time with Shorthands

### Exercise 3 Time to Practice - Reactive Properties

### Sec 2-19 Dynamic Styling with CSS Classes-Basics

### Sec 2-20 Dynamic Styling with CSS Classes-Using Names

### Sec 2-21 Setting Styles Dynamically (without CSS Classes)

### Sec 2-22 Styling Elements with the Array Syntax

### Exercise 4 Time to Practice - Styling

### Sec 2-23 Module Wrap Up

### Sec 2-4 Module Resource & Useful Links

-----



