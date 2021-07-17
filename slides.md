---
theme: seriph
background: https://source.unsplash.com/1920x1080?abstract,blue
class: text-center
highlighter: shiki
info: |
  ## Vue Masterclass to Develop Real-life Web Applications
  
  ### Details:
  From July 31st

  Every Saturday and Sunday at 7.30 pm

  ### Trainer:
  Mir Ayman Ali
  
  Senior Software Engineer

  Learn more at [upskill.com.bd](https://upskill.com.bd/workshop/253)

title: Vue Masterclass | Preview
---
<div class="flex justify-center">
  <logos-vue class="text-6xl" />
</div>
 

# <span> Vue Masterclass <small>(with Ayman)</small> </span>

Presentation slides for developers

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Let's Begin <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <a href="https://github.com/alimirayman/upskill-vue-initial" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
layout: cover

---
<div class="flex justify-center">
  <div class="rounded-full h-32 w-32 flex items-center justify-center bg-cover" style="background-image: url('https://avatars.githubusercontent.com/u/3832930?v=4')">
  </div>
</div>

## Mir Ayman Ali

<div class="flex justify-center gap-2">
  <a href="https://github.com/alimirayman" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
  <a href="https://www.linkedin.com/in/alimirayman/" target="_blank" alt="LinkedIn"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-linkedin />
  </a>
</div>

<div class="flex pt-6 justify-around text-sm mx-20">
  <div class="bg-gradient-to-r from-green-400 to-blue-500 hover:from-pink-500 hover:to-yellow-500 p-2 rounded" v-click>
    Senior Software Engineer
    @
    <a href="https://www.obviously.ai/" target="_blank">Obviously.ai</a>
  </div>
  <div class="bg-gradient-to-r from-green-400 to-blue-500 hover:from-pink-500 hover:to-yellow-500 p-2 rounded" v-click>
    Co-Founder | CEO
    @
    <a href="https://shastho.ai/" target="_blank">Shastho.ai</a>
  </div>
</div>


---

<div class="flex justify-start align-center"> 
  <h1>Why Vue JS?</h1>
  <logos-vue class="text-4xl pl-3" />
</div>

The Progressive JavaScript Framework

- 🚀 **Easier Learning Curve** - Easy to get in, learn and Impliment
- 🤡 **Simple** - Easy to use
- 📝 **Awesome Documentation** - Can learn just by going through the docs
- ⚡️ **High Performance** - Page loads very fast 😜
- 👥 **Vibrant Community** - Huge communnity so you don't feel stuck
- 🕸 **SPA / SSR** - Single Page Application & Server Side Renderinng

<br>
<br>

Read more about [Vue](https://vuejs.org/)

---

# Why this Course?

- Learn deep into frontend
- Potential job opportunity
- Learn from a prefessional

<br>
<br>

---
layout: section
---

# Code

---

# Basic Vue File (.vue)

```html {all|1-3|5-9|10-13|all}
<template>
  <!-- html -->
</template>

<script>
export default {
// JS
}
</script>

<style>
  /* CSS */
</style>

```

---

# Job Cards (Old Style)

### Code

```html 
<div class="flex justify-around mt-6 text-sm mx-20">
  <div class="bg-gradient-to-r from-green-400 to-blue-500 hover:from-pink-500 hover:to-yellow-500 p-2 rounded" v-click>
    Senior Software Engineer
    @
    <a href="https://www.obviously.ai/" target="_blank">Obviously.ai</a>
  </div>
  <div class="bg-gradient-to-r from-green-400 to-blue-500 hover:from-pink-500 hover:to-yellow-500 p-2 rounded" v-click>
    Co-Founder | CEO
    @
    <a href="https://shastho.ai/" target="_blank">Shastho.ai</a>
  </div>
</div>
```

### Result

<div class="flex pt-6 justify-around text-sm mx-20">
  <div class="bg-gradient-to-r from-green-400 to-blue-500 hover:from-pink-500 hover:to-yellow-500 p-2 rounded" >
    Senior Software Engineer
    @
    <a href="https://www.obviously.ai/" target="_blank">Obviously.ai</a>
  </div>
  <div class="bg-gradient-to-r from-green-400 to-blue-500 hover:from-pink-500 hover:to-yellow-500 p-2 rounded" >
    Co-Founder | CEO
    @
    <a href="https://shastho.ai/" target="_blank">Shastho.ai</a>
  </div>
</div>

---

# Job Card Component (.vue)

### Code

```html {all|3,12|5,13,14|all}
<template>
  <div class="bg-gradient-to-r from-green-400 to-blue-500 hover:from-pink-500 hover:to-yellow-500 p-2 rounded" >
    {{ jobTitle }}
    @
    <a :href="companyURL" target="_blank">{{ companyName }}</a>
  </div>
</template>

<script>
export default {
  props: {
    jobTitle: String,
    companyURL: String,
    companyName: String,
  }
}
</script>
```

---


# Job Card Component (.vue)

### Usage

```html {all|1-5|6-10|all}
<JobCard 
  jobTitle="Sennior Software Engineer"
  companyURL="https://www.obviously.ai/"
  companyName="Obviously.ai"
/>
<JobCard 
  jobTitle="Co-Founder | CEO"
  companyURL="https://shastho.ai/"
  companyName="Shastho.ai"
/>
```

### Result

<!-- ./components/JobCard.vue -->
<div class="flex pt-6 justify-around text-sm mx-20">
<JobCard 
  jobTitle="Sennior Software Engineer"
  companyURL="https://www.obviously.ai/"
  companyName="Obviously.ai"
  v-click="1"
/>
<JobCard 
  jobTitle="Co-Founder | CEO"
  companyURL="https://shastho.ai/"
  companyName="Shastho.ai"
  v-click="2"
/>
</div>

---

# Components

<div grid="~ cols-2 gap-4">
<div>

```html
<Counter :count="10" />
```

<!-- ./components/Counter.vue -->
<Counter :count="10" m="t-4" />

<br/>
<br/>

```html
<Counter :count="25" offset="2" />
```

<!-- ./components/Counter.vue -->
<Counter :count="25" offset="2" m="t-4" />

<br/>
<br/>

```html
<Counter :count="32" offset="3" />
```

<!-- ./components/Counter.vue -->
<Counter :count="32" offset="3" m="t-4" />

</div>
<div>

```html
<Tweet id="1407635397887287298" />
```

<Tweet id="1407635397887287298" scale="0.65" />

</div>
</div>


---
layout: center
class: text-center
---

# Learn More

[Documentations](https://vuejs.org/v2/guide/) · [GitHub](https://github.com/alimirayman/upskill-vue-initial)
