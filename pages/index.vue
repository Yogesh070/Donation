<template>
  <div class="home">
    <img src="../assets/logo.jpg" alt="logo" />
    <h1>Kishor Trust</h1>
    <NuxtLink to="/donate"><button>Dontate Now</button></NuxtLink>
    <NuxtLink to="/NewDonation"><button>New Dontation</button></NuxtLink>
    <NuxtLink to="/Condolence"><button>Condolence</button></NuxtLink>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;700;800&display=swap");
body {
  background-color: #fcfcfc;
}
.home {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  font-family: "Open Sans", sans-serif;
  background-color: #fcfcfc;
}
h1 {
  font-weight: 800;
  margin-bottom: 2rem;
  padding: 2rem;
}
img {
  max-height: 210px;
  max-width: 250px;
}
button {
  padding: 10px 12px;
  border: none;
  color: white;
  background-color: #77aca2;
  border-radius: 5px;
  outline: none;
  cursor: pointer;
  font-size: 1rem;
  margin-bottom: 1rem;
}
button:hover {
  opacity: 0.8;
}
</style>