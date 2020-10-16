<template>
  <div id="main">
    <nav v-bind:class="active" v-on:click.prevent>
      <a href="#" class="home" v-on:click="makeActive('home')">Home</a>
      <a href="#" class="projects" v-on:click="makeActive('cause')"
        >Our cause</a
      >
      <a href="#" class="services" v-on:click="makeActive('services')"
        >Services</a
      >
      <a href="#" class="contact" v-on:click="makeActive('contact')">Contact</a>
    </nav>
  </div>
</template>

<script>
export default {
  data() {
    return {
      active: true,
    };
  },
  methods: {
    makeActive: function (item) {
      // When a model is changed, the view will be automatically updated.
      this.active = item;
    },
  },
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
}

body {
  font: 15px/1.3 "Open Sans", sans-serif;
  color: #5e5b64;
  text-align: center;
}

a,
a:visited {
  outline: none;
  color: #389dc1;
}

a:hover {
  text-decoration: none;
}

section,
footer,
header,
aside,
nav {
  display: block;
}

/*-------------------------
	The menu
--------------------------*/
#main {
  width: 100%;
}
nav {
  display: flex;
  justify-content: flex-end;
  padding: 2rem;
  background-image: url("https://explorer.compassion.com/wp-content/uploads/2018/04/1706_TH0812_179.png");
  opacity: 0.9;
  background-size: cover;
  background-position: center;
  /* margin-bottom: 3rem; */
  box-shadow: 0 1px 1px #ccc;
  border-radius: 2px;
}

nav a {
  display: inline-block;
  padding: 18px 30px;
  color: #fff !important;
  font-weight: bold;
  font-size: 16px;
  text-decoration: none !important;
  line-height: 1;
  text-transform: uppercase;
  background-color: transparent;

  -webkit-transition: background-color 0.25s;
  -moz-transition: background-color 0.25s;
  transition: background-color 0.25s;
}

nav a:first-child {
  border-radius: 2px 0 0 2px;
}

nav a:last-child {
  border-radius: 0 2px 2px 0;
}

nav.home .home,
nav.projects .projects,
nav.services .services,
nav.contact .contact {
  background-color: #e35885;
}

p {
  font-size: 22px;
  font-weight: bold;
  color: #7d9098;
}

p b {
  color: #ffffff;
  display: inline-block;
  padding: 5px 10px;
  background-color: #c4d7e0;
  border-radius: 2px;
  text-transform: uppercase;
  font-size: 18px;
}
</style>