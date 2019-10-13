<template>
  <header>
    <div class="header-container">
      <p class="intro heading">{{ hello }}</p>
      <p class="intro sub-heading">{{ greeting }}</p>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      helloHolder: "Hello,",
      greetingHolder: "I'm Dami",
      pos: 0,
      pos2: 0,
      hello: "",
      greeting: ""
    };
  },
  methods: {
    update: function() {
      if (this.helloHolder !== this.hello) {
        this.hello += this.helloHolder[this.pos];
        this.pos++;
      } else if (this.pos2 < this.greetingHolder.length) {
        this.greeting += this.greetingHolder[this.pos2];
        this.pos2++;
      }
    }
  },
  created: function() {
    let timerId = setInterval(() => {
      this.update();
    }, 100);
    setTimeout(() => {
      clearInterval(timerId);
    }, 5000);
  }
};
</script>
<style>
header {
  height: 100%;
  display: flex;
  align-items: flex-end;
  flex-direction: row;
}
</style>
<style scoped>
.intro {
  font-weight: 500;
  font-size: 7em;
  color: white;
  margin-left: 50px;
}

.heading {
  flex-grow: 1;
  margin-bottom: 0;
}
.sub-heading {
  height: 50px;
  flex-grow: 0;
  margin-top: 80px;
  margin-bottom: 100px;
}
@media only screen and (max-width: 575px) {
  .intro {
    margin-left: 20px;
    font-weight: 200;
    font-size: 5em;
  }
  .sub-heading {
    margin-top: 40px;
  }
}

@media only screen and (max-width: 330px) {
  .intro {
    margin-left: 20px;
    margin-bottom: 50px;
    font-weight: 200;
    font-size: 4em;
  }
  .heading {
    margin-bottom: 0px;
  }
  .sub-heading {
    margin-top: 30px;
  }
}
</style>