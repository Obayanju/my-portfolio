<template>
  <header>
    <p class="intro">
      Hello,<br />
      I'm Dami
    </p>
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
  font-weight: 500;
  font-size: 7em;
  color: white;
  flex-grow: 6;
  margin-left: 50px;
  margin-bottom: 100px;
  line-height: 0.9em;
}

@media only screen and (max-width: 500px) {
  .intro {
    margin-left: 20px;
    font-weight: 200;
    font-size: 5em;
  }
}

@media only screen and (max-width: 330px) {
  .intro {
    margin-left: 20px;
    margin-bottom: 50px;
    font-weight: 200;
    font-size: 4em;
  }
}
</style>