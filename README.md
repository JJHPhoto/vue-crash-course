# [Vue JS Crash Course](https://www.youtube.com/watch?v=qZXt1Aom3Cs)

I'm trying to learn Vue JS for some contract work, so I decided to go through Traversy's course on YouTube. I find him to be one of the best and most thorough trainers.

At the beginning, there was an interesting project to get familiar with how easy it is to use Vue. I really liked when Traversy showed the _normal_ way to do something and then the Vue way. For instance, the shortened syntax for `v-bind:` being `:`.

I continue to enjoy that Traversy shows you things that you're not going to use, like `vue ui `, in the project. Just to let you know it's there.

## Task Manager

One of the things I enjoy with coding is learning through errors. I received this error on my Tasks component:

```
[vue/no-multiple-template-root]
The template root disallows 'v-for' directives.eslint-plugin-vue
```

Since I got this error while creating a task list on my App component, I thought this error was preventing me from rendering the list. So I worked out a fix for that error but the list was still not rendering. I then realized I had capitalized

```
    <Tasks :tasks="Tasks" />
```

here, but it should have just been like this:

```
    <Tasks :tasks="tasks" />
```

Once I had that "working", I wondered if the solution I had found for the previous error was still necessary. I had added an empty `<div>` inside the `<template>` so that the `v-for` div wasn't at the root of the template. Turns out that error doesn't prevent the component from working. It appears to just be an eslint warning that doesn't break my code. Good to know! And to learn!

While working through the "delete-task" part of the app, I liked that Traversy would console.log things to see if it was working. Then move on once it logged. Its a very simple check but I sometimes forget how easy it is to check things that way.
