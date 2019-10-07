<template>
  <fieldset>
    <legend class="title">
      <h3>{{ content.title }}</h3>
    </legend>
    <div class="field">
      {{ content.body }}
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
fieldset {
  margin: 20px 15px;
  border-radius: 8px;
  border: 2px solid;
  line-height: 2em;
}
.title h3 {
  color: purple;
  cursor: pointer;
}
.field {
  color: white;
}
</style>