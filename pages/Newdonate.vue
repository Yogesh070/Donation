<template>
  <div class="donate">
    <Navbarvue />
    <div class="donation-box">
      <div class="donation-container">
        <div class="image-container"></div>
        <div class="donation-text">
          <h4>You are donating to:</h4>
          <h1>Providing access to safe water, sanitation, and hygiene</h1>
          <p>
            The legal definition of a charitable organization (and of charity)
            varies between countries
          </p>
          <div class="donation-bar">
            <!-- <span></span> -->
            <h3>45% Donated</h3>
            <h3>Goal:$3000000</h3>
          </div>
        </div>
      </div>
      <Payment />
    </div>
    <div></div>
    <!-- <Login /> -->
    <Footer />
  </div>
</template>

<script>
import Navbarvue from "../components/NavbarVue";
import Payment from "../components/Payment";
import Login from "../components/loginform";
import Footer from "../components/Footer";
export default {
  components: {
    Navbarvue,
    Payment,
    Footer,
    Login,
  },
};
</script>

<style scoped>
.donation-box {
  height: 40vh;
  background-color: #05d192;
  display: flex;
  justify-content: center;
}

.donation-container {
  display: flex;
  font-family: "Poppins", sans-serif;
  max-width: 73rem;
  margin: 4rem;
}
.donation-text {
  padding: 0 2rem;
}
.donation-text h1 {
  color: #383838;
  line-height: 34px;
  font-weight: 500;
}
.donation-text p {
  color: #5e5e5e;
  padding: 1rem 0;
}
.donation-bar {
  display: flex;
  justify-content: space-between;
  margin-bottom: 1rem;
}
.image-container {
  max-width: 400px;
  width: 100%;
  background-image: url(https://demo.goodlayers.com/chariti/demo1/wp-content/uploads/sites/2/2016/06/larm-rmah-AEaTUnvneik-unsplash-1200x755.jpg);
  background-size: cover;
}
@media (max-width: 900px) {
  .donation-container {
    margin: 0;
  }
}
@media (max-width: 1235px) {
  .image-container {
    width: 0;
  }
}
@media (max-width: 600px) {
  .donation-text {
    padding: 2rem;
  }
}
</style>