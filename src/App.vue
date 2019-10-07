<template>
  <div id="app">
    <Navigation />
    <Hero />
    <div id="container">
      <Field
        v-for="(section, index) in sections"
        v-bind:content="section"
        :key="index"
      />
    </div>
  </div>
</template>

<script>
import Hero from "./components/Hero.vue";
import Navigation from "./components/Navigation.vue";
import Field from "./components/Field.vue";
import FieldContainer from "./components/FieldContainer.vue";
export default {
  name: "app",
  components: {
    Hero,
    Navigation,
    Field,
    FieldContainer
  },
  data() {
    return {
      sections: [
        {
          title: "About",
          body: `Quisque ac fringilla ex. Praesent blandit mattis augue,
       non tristique sem bibendum a. Donec in posuere ex, iaculis
       mattis sapien. Donec et ex congue, congue mi et, sagittis
       mi. Aliquam ac ex nisl. Proin ullamcorper mollis felis ac
       dictum. Suspendisse porttitor nulla eget dignissim maximus.
       Nullam ut gravida tortor, quis pharetra leo. Aliquam nec
       consectetur lectus, sed congue libero. Integer vulputate,
       justo quis iaculis lacinia, nulla sem pharetra felis, vitae
       sodales neque ipsum pellentesque ante. Aliquam egestas
       dui in pretium fermentum. Phasellus auctor est est.
       `
        },
        {
          title: "Experience",
          body: `Quisque ac fringilla ex. Praesent blandit mattis augue,
       non tristique sem bibendum a. Donec in posuere ex, iaculis
       mattis sapien. Donec et ex congue, congue mi et, sagittis
       mi. Aliquam ac ex nisl. Proin ullamcorper mollis felis ac
       dictum. Suspendisse porttitor nulla eget dignissim maximus.
       Nullam ut gravida tortor, quis pharetra leo. Aliquam nec
       consectetur lectus, sed congue libero. Integer vulputate,
       justo quis iaculis lacinia, nulla sem pharetra felis, vitae
       sodales neque ipsum pellentesque ante. Aliquam egestas
       dui in pretium fermentum. Phasellus auctor est est.
       `
        },
        {
          title: "Resumé",
          body: `Quisque ac fringilla ex. Praesent blandit mattis augue,
       non tristique sem bibendum a. Donec in posuere ex, iaculis
       mattis sapien. Donec et ex congue, congue mi et, sagittis
       mi. Aliquam ac ex nisl. Proin ullamcorper mollis felis ac
       dictum. Suspendisse porttitor nulla eget dignissim maximus.
       Nullam ut gravida tortor, quis pharetra leo. Aliquam nec
       consectetur lectus, sed congue libero. Integer vulputate,
       justo quis iaculis lacinia, nulla sem pharetra felis, vitae
       sodales neque ipsum pellentesque ante. Aliquam egestas
       dui in pretium fermentum. Phasellus auctor est est.
       `
        },
        {
          title: "Projects",
          body: `Quisque ac fringilla ex. Praesent blandit mattis augue,
       non tristique sem bibendum a. Donec in posuere ex, iaculis
       mattis sapien. Donec et ex congue, congue mi et, sagittis
       mi. Aliquam ac ex nisl. Proin ullamcorper mollis felis ac
       dictum. Suspendisse porttitor nulla eget dignissim maximus.
       Nullam ut gravida tortor, quis pharetra leo. Aliquam nec
       consectetur lectus, sed congue libero. Integer vulputate,
       justo quis iaculis lacinia, nulla sem pharetra felis, vitae
       sodales neque ipsum pellentesque ante. Aliquam egestas
       dui in pretium fermentum. Phasellus auctor est est.
       `
        },
        {
          title: "Contacts",
          body: `Quisque ac fringilla ex. Praesent blandit mattis augue,
       non tristique sem bibendum a. Donec in posuere ex, iaculis
       mattis sapien. Donec et ex congue, congue mi et, sagittis
       mi. Aliquam ac ex nisl. Proin ullamcorper mollis felis ac
       dictum. Suspendisse porttitor nulla eget dignissim maximus.
       Nullam ut gravida tortor, quis pharetra leo. Aliquam nec
       consectetur lectus, sed congue libero. Integer vulputate,
       justo quis iaculis lacinia, nulla sem pharetra felis, vitae
       sodales neque ipsum pellentesque ante. Aliquam egestas
       dui in pretium fermentum. Phasellus auctor est est.
       `
        }
      ]
    };
  }
};
</script>

<style>
html,
body {
  height: 100%;
  margin: 0;
  padding: 0;
  line-height: 3.1em;
}
body {
  background-color: #252628;
}
#app {
  font-family: "avenir", helvetica, arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  height: 100%;
}
#container {
  margin: 0 auto;
  max-width: 1200px;
}
</style>
