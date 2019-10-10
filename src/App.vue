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
    <Footer />
  </div>
</template>

<script>
import Hero from "./components/Hero.vue";
import Navigation from "./components/Navigation.vue";
import Field from "./components/Field.vue";
import FieldContainer from "./components/FieldContainer.vue";
import Footer from "./components/Footer.vue";
export default {
  name: "app",
  components: {
    Hero,
    Navigation,
    Field,
    FieldContainer,
    Footer
  },
  data() {
    return {
      prevScrollPos: null,
      currScrollPos: null,
      sections: [
        {
          title: "About",
          type: "about",
          body: `I'm a computer science major in my 4th year,
          and currently a teaching assistant for Programming
          in C++ CS3005. I got introduced to programming after graduating from high
          school, and have been hooked ever since. These days I'm juggling school work,
           side projects, and being a teaching assistant.`
        },
        {
          title: "Experience",
          type: "experience",
          body: `Voluntary Teaching Assistant - Dixie State University`
        },
        {
          title: "Selected Projects",
          type: "project",
          body: ``
        },
        {
          title: "Contacts",
          type: "contact",
          body: `I'm currently in search of Internship for the summer of 2020. Get in touch with me!`
        }
      ]
    };
  },
  methods: {
    handleScroll() {
      this.currScrollPos = window.pageYOffset;
      if (this.prevScrollPos > this.currScrollPos) {
        document.getElementById("navbar").style.top = "0";
      } else {
        document.getElementById("navbar").style.top = "-160px";
      }
      this.prevScrollPos = this.currScrollPos;
    }
  },
  created() {
    this.prevScrollPos = window.pageYOffset;
    window.addEventListener("scroll", this.handleScroll);
  },
  destroyed() {
    window.removeEventListener("scroll", this.handleScroll);
  }
};
</script>

<style>
html {
  scroll-behavior: smooth;
}
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
#container,
footer {
  margin: 0 auto;
  max-width: 900px;
}
</style>
