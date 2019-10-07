<template>
  <nav class="navbar">
    <a href="/" class="title">Damilare Obayanju</a>
    <ul class="links">
      <a href="">About</a>
      <a href="">Experience</a>
      <a href="">Resume</a>
      <a href="">Projects</a>
      <a href="">Contacts</a>
    </ul>
  </nav>
</template>

<script>
export default {};
</script>
<style >
.navbar {
  background-color: #252628;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  position: fixed;
  padding-left: 10px;
  width: 100%;
}
.links {
  margin: 0;
  padding-right: 5px;
  padding-left: 0;
}
.links a {
  color: white;
  padding-right: 10px;
  text-decoration: none;
}
.links a:hover {
  color: yellow;
}
.links a:last-child {
  padding-right: 30px;
}
nav .title {
  color: white;
  text-decoration: none;
}
</style>