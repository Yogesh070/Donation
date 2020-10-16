<template>
  <div class="donate">
    <h1>Donate Now</h1>
    <p>
      We are only able to carry on our work through the generosity of
      individuals, institutions and people like you. Please take the time to
      make a donation. We value every gift we receive and ensure that your money
      goes straight to where it is needed most. Help us make a difference to the
      people of the ‘Hidden Himalayas’ by selecting one of the options below.
    </p>
    <DonateContainer
      v-for="post in posts"
      :key="post.title"
      v-bind:title="post.title"
      v-bind:description="post.description"
      v-bind:image="post.image"
    />
  </div>
</template>

<script>
import DonateContainer from "../components/DonateContainer";
import jsonposts from "./posts.json";
export default {
  components: {
    DonateContainer,
  },
  data() {
    return {
      posts: jsonposts,
    };
  },
};
</script>

<style scoped>
.donate {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: #e2e2e2;
}
.donate > p {
  font-size: 1.3rem;
  max-width: 1200px;
  padding: 2rem;
}
.donate h1 {
  font-weight: 800;
  font-size: 4rem;
  color: #3c9787;
}
</style>