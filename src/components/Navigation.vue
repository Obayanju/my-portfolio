<template>
  <nav id="navbar">
    <a href="/" class="title">Damilare Obayanju</a>
    <ul class="links">
      <button class="resume">Resumé</button>
      <a href="#about">About</a>
      <a href="#experience">Experience</a>
      <a href="#project">Projects</a>
      <a href="#contact">Contacts</a>
    </ul>
    <!-- <div>Icons made by <a href="https://www.flaticon.com/authors/dave-gandy" title="Dave Gandy">Dave Gandy</a> from <a href="https://www.flaticon.com/"             title="Flaticon">www.flaticon.com</a></div> -->
  </nav>
</template>

<script>
export default {};
</script>
<style >
#navbar {
  background-color: #252628;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  position: fixed;
  padding-left: 10px;
  width: 100%;
  transition: top 0.3s;
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
  color: #0069ed;
}
.links a:last-child {
  padding-right: 30px;
}
nav .title {
  color: white;
  text-decoration: none;
  margin: 10px;
}

.resume {
  display: inline-block;
  border: none;
  padding: 1rem 1rem;
  margin: 10px 10px;
  text-decoration: none;
  background: #0069ed;
  color: #ffffff;
  font-size: 1rem;
  cursor: pointer;
  text-align: center;
  transition: background 250ms ease-in-out, transform 150ms ease;
  -webkit-appearance: none;
  -moz-appearance: none;
}

.resume:hover,
.resume:focus {
  background: #0053ba;
}

.resume:focus {
  outline: 1px solid #fff;
  outline-offset: -4px;
}

.resume:active {
  transform: scale(0.99);
}

@media only screen and (max-width: 500px) {
  #navbar {
    justify-content: center;
  }
  .links {
    display: flex;
  }
  .resume {
    margin: 0 10px 0 0;
  }
}

@media only screen and (max-width: 330px) {
  .links {
    width: 100%;
    flex-wrap: wrap;
    justify-content: center;
  }
  .title,
  .resume,
  .links {
    font-size: 0.7rem;
  }
}
</style>