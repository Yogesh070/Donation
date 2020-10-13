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
export default {
  components: {
    DonateContainer,
  },
  data() {
    return {
      posts: [],
      // posts: [
      //   {
      //     title: "Healthcare & Opportunity in the Hidden Himalayas",
      //     description:
      //       "This project provides basic healthcare -and education in the least developed area of Nepal. There are no roads in Humla and the government health system is dysfunctional. Maternal and child mortality rates are some of the highest in the world (<30%). More than 50,000 people live in the district. The project is integrated with education, food security, WASH, renewable energy and income generation projects to promote a healthier lifestyle and a secure future for, particularly, women and children.",
      //     image:
      //       "https://www.nepaltrust.org/wp-content/uploads/2019/02/health-picture.jpg",
      //   },
      //   {
      //     title: "The 100% Project",
      //     description:
      //       "The Nepal Trust is working in the district of Baglung in West Nepal with local organisations Daughlagiri Intergrated Rural Development Centre DIRDC and the Nepal Development Foundation to tackle and eradicate the illegal and dangerous practice of Chhaupadi. During their monthly period woman and girls are exiled from their homes and schools to unhygienic cow sheds or similar. They are considered unclean and a danger to the fragile purity of the home and traditional culture.",
      //     image:
      //       "https://www.nepaltrust.org/wp-content/uploads/2020/08/pict_large.png",
      //   },
      // ],
    };
  },
  methods: {
    getPost() {
      fetch("posts.json")
        .then((response) => response.json())
        .then((data) => (this.posts = data));
      console.log(this.posts);
    },
  },
  beforeMount() {
    this.getPost();
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