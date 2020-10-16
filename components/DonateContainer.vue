<template>
  <div class="donateContainer">
    <img :src="image" alt="image" />
    <div class="content">
      <h1>{{ title }}</h1>
      <p>{{ description }}</p>
      <NuxtLink to="/transaction" v-bind:topic="title"
        ><button>Donate Now</button></NuxtLink
      >
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    description: String,
    image: String,
  },
};
</script>

<style scoped>
.donateContainer {
  display: flex;
  margin: 2rem 0;
  max-width: 1200px;
  margin: 2rem;
}
.content {
  margin: 0 2rem;
}
.content p {
  padding: 1rem 0;
  font-size: 1.2rem;
}
img {
  object-fit: contain;
  max-height: 266px;
  max-width: 400px;
}
h1 {
  color: #40454f;
}
button {
  padding: 10px 12px;
  border: none;
  color: white;
  background-color: #3c9787;
  border-radius: 5px;
  outline: none;
  cursor: pointer;
  font-size: 1rem;
}
@media only screen and (max-width: 900px) {
  .donateContainer {
    flex-wrap: wrap;
  }
  .content {
    margin: 0;
  }
}
</style>