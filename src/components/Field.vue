<template>
  <fieldset>
    <legend class="title">
      <h3 class="field-title">{{ content.title }}</h3>
    </legend>
    <div class="field">
      {{ content.body }}
      <div v-if="content.type == 'experience'">
        August 2019 - Present
        <ul>
          <li>
            Assiting the professor in answering students questions about
            homeworks
          </li>
          <li>
            Oraganized lab hours to help students with questions about the
            course
          </li>
        </ul>
      </div>
      <div v-if="content.type == 'project'">
        <h3>
          <a
            class="title"
            href="https://github.com/job-app-tracker/job-app-tracker"
            >Job Application Tracker</a
          >
        </h3>
        <p>
          An application to help organize the job hunting process by keeping
          track of jobs as wishlists, applied, offer, or rejected.
        </p>
        <ul class="technologies">
          <small>Vue</small>
          <small>Express</small>
          <small>MongoDB</small>
          <small>Mongoose</small>
          <small>HTML & CSS</small>
          <small>Node.js</small>
          <small>Heroku</small>
        </ul>
        <h3>
          <a class="title" href="https://github.com/Obayanju/felastab"
            >JavaScript Interpreter</a
          >
        </h3>
        <p>
          An interpreter that parses JavaScript code, evaluates it and produces
          the expected output.
        </p>
        <ul class="technologies">
          <small>Go</small>
        </ul>
      </div>
      <div class="contact-container" v-if="content.type == 'contact'">
        <button class="contact-me">Contact Me!</button>
      </div>
    </div>
  </fieldset>
</template>

<script>
export default {
  name: "Field",
  props: ["content"]
};
</script>

<style>
.technologies {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  list-style: none;
  padding-left: 0;
}
.technologies small {
  padding: 0 20px 0 0;
}
h3 {
  margin: 0;
}
h3 .title {
  text-decoration: none;
  color: white;
}
fieldset {
  margin: 20px 15px;
  border-radius: 8px;
  border: 2px solid;
  line-height: 2em;
}
.field-title {
  color: #0069ed;
  cursor: pointer;
}
.title {
  height: 30px;
}

.field {
  color: white;
}
.contact-container {
  margin: 50px 0;
}
.contact-me {
  display: inline-block;
  border: none;
  padding: 1rem 2rem;
  margin: 0 50%;
  text-decoration: none;
  background: #0069ed;
  color: #ffffff;
  font-family: sans-serif;
  font-size: 1rem;
  cursor: pointer;
  text-align: center;
  transition: background 250ms ease-in-out, transform 150ms ease;
  -webkit-appearance: none;
  -moz-appearance: none;
}

.contact-me:hover,
.contact-me:focus {
  background: #0053ba;
}

.contact-me:focus {
  outline: 1px solid #fff;
  outline-offset: -4px;
}

.contact-me:active {
  transform: scale(0.99);
}
</style>