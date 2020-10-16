<template>
  <div class="donate">
    <NavbarVue />
    <div class="donation-container">
      <div class="image-container"></div>
      <div class="donation-text">
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
        <div class="donation-status">
          <div>
            <h2 class="donor">71</h2>
            <span>Donor</span>
          </div>
          <div>
            <h2 class="amount">$13,565.00</h2>
            <span>Donation</span>
          </div>
        </div>
        <div class="social-box">
          <img
            src="../assets/social-icon/facebook-f-brands.svg"
            alt="facebooklogo"
          />
          <img src="../assets/social-icon/instagram-brands.svg" alt="insta" />
          <img
            src="../assets/social-icon/pinterest-p-brands.svg"
            alt="pininterest"
          />
          <img src="../assets/social-icon/twitter-brands.svg" alt="twitter" />
        </div>
        <div class="button-box">
          <NuxtLink to="/Newdonate"><button>Donate Now</button></NuxtLink>
          <button class="follow">Follow</button>
        </div>
      </div>
    </div>
    <div class="content">
      <h1>How did this come to our attention?</h1>
      <p>
        During the 19th century a profusion of charitable organizations emerged
        to alleviate the awful conditions of the working class in the slums. The
        Labourer’s Friend Society, chaired by Lord Shaftesbury in the United
        Kingdom in 1830, aimed to improve working-class conditions. It promoted,
        for example, the allotment of land to labourers for “cottage husbandry”
        that later became the allotment movement. In 1844 it became the first
        Model Dwellings Company. There was strong growth in municipal charities.
        The Brougham Commission led on to the Municipal Corporations Act 1835,
        which reorganized multiple local charities by incorporating them into
        single entities under supervision from local government.
      </p>
      <div class="content-two">
        <h1>
          Clean water, sanitation, and hygiene education are basic necessities
          for a healthy environment and a productive life and well life being
        </h1>
        <div class="stats">
          <div>
            <img
              src="https://demo.goodlayers.com/chariti/demo1/wp-content/uploads/sites/2/2020/02/cause-icon-menwomen.png"
              alt=""
            />
            <h1>100K</h1>
            <p>Children Helped</p>
          </div>
          <div>
            <img
              src="https://demo.goodlayers.com/chariti/demo1/wp-content/uploads/sites/2/2020/02/cause-icon-hand.png"
              alt=""
            />
            <h1>18000</h1>
            <p>Volunterrs Worldwide</p>
          </div>
          <div>
            <img
              src="https://demo.goodlayers.com/chariti/demo1/wp-content/uploads/sites/2/2020/02/cause-icon-clush.png"
              alt=""
            />
            <h1>$100M</h1>
            <p>Fund Raised</p>
          </div>
        </div>
        <p>
          During the 19th century a profusion of charitable organizations
          emerged to alleviate the awful conditions of the working class in the
          slums. The Labourer’s Friend Society, chaired by Lord Shaftesbury in
          the United Kingdom in 1830, aimed to improve working-class conditions.
        </p>
        <div class="goals">
          <ul>
            <li>
              <span
                ><img
                  src="../assets/check-circle-regular.svg"
                  alt="checkicon" /></span
              >Provide long-term campaign planning
            </li>
            <li>
              <span
                ><img
                  src="../assets/check-circle-regular.svg"
                  alt="checkicon" /></span
              >Reduce our long term administration costs
            </li>
            <li>
              <span
                ><img
                  src="../assets/check-circle-regular.svg"
                  alt="checkicon" /></span
              >Provide long-term campaign planning
            </li>
            <li>
              <span
                ><img
                  src="../assets/check-circle-regular.svg"
                  alt="checkicon" /></span
              >Reduce our long term administration costs
            </li>
          </ul>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>
<script>
import Navbarvue from "../components/NavbarVue";
import Footer from "../components/Footer";

export default {
  components: {
    Navbarvue,
    Footer,
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@100;400;700;900&display=swap");
.donate {
  display: flex;
  /* justify-content: center; */
  align-items: center;
  flex-direction: column;
}
.donation-container {
  margin-top: 3rem;
  display: flex;
  font-family: "Poppins", sans-serif;
}
.donation-text {
  padding: 2rem;
}
.donation-text h1 {
  color: #383838;
  line-height: 34px;
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
.social-box {
  margin: 2rem 0;
}
.social-box img {
  height: 18px;
  margin-right: 15px;
  color: #383838;
}
.image-container {
  max-width: 900px;
  width: 100%;
  min-height: 400px;
  background-image: url(https://demo.goodlayers.com/chariti/demo1/wp-content/uploads/sites/2/2016/06/larm-rmah-AEaTUnvneik-unsplash-1200x755.jpg);
  background-size: cover;
}
/* .image-container img {
  width: 100%;
  height: 100%;
} */
.button-box button {
  padding: 0.9rem 1.2rem;
  color: white;
  font-size: 0.9rem;
  border: none;
  background-color: #05d192;
  font-weight: 900;
  outline: none;
  cursor: pointer;
}
.button-box .follow {
  background-color: white;
  color: #05d192;
  border: 2px solid #05d192;
  padding: 0.8rem;
}
.donation-status {
  display: flex;
  justify-content: space-between;
  padding-top: 1rem;
  border-top: 1px solid #c4c3c3;
}
.donation-status span {
  color: #5e5e5e;
}
.content {
  max-width: 81rem;
  padding: 2rem;
}
.content h1 {
  font-size: 24px;
  font-weight: 900;
}
.content p {
  line-height: 1.5;
  font-size: 18px;
  color: #5e5e5e;
  margin: 2rem 0;
}
.content-two > h1 {
  border-top: 2px solid #05d192;
  color: #05d192;
  padding-top: 2rem;
}
.content-two .stats {
  display: flex;
  justify-content: space-around;
  margin: 2rem 0;
}
.content-two .stats p {
  margin: 0;
}
.content-two .stats div {
  text-align: center;
}
.goals {
  line-height: 1.5;
  font-size: 20px;
  color: #5e5e5e;
}
.goals li {
  list-style: none;
}
.goals li span img {
  height: 20px;
  margin-right: 10px;
}
@media only screen and (max-width: 900px) {
  .donation-container {
    flex-wrap: wrap;
  }
}
</style>