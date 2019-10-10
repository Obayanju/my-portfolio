<template>
  <header>
    <h1 class="intro">
      Hello,<br />
      I'm Dami
    </h1>
  </header>
</template>

<script>
export default {
  name: "Header"
};
</script>
<style>
header {
  height: 100%;
  display: flex;
  align-items: flex-end;
}
</style>
<style scoped>
.intro {
  color: white;
  flex-grow: 6;
  margin-left: 50px;
  font-size: 7em;
  line-height: 0.9em;
}

.intro {
  margin-bottom: 100px;
}
</style>