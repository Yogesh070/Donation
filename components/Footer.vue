<template>
  <div class="footer-container">
    <div class="footer">
      <div class="footer-top">
        <div class="container">
          <h2>VOICES</h2>
          <p>
            Lorem ipsum dolor, sit amet consectetur adipisicing elit.
            Asperiores, sit labore illum, odio, ex autem molestias voluptatum
            quae placeat qui veritatis libero? Repellat, similique vitae!
          </p>
          <a href="">Lorem ipsr.</a>
        </div>
        <div class="container">
          <h2>HOW WE FUND</h2>
          <p>
            Lorem ipsum dolor, sit amet consectetur adipisicing elit.
            Asperiores, sit labore illum, odio, ex autem molestias voluptatum
            quae placeat qui veritatis libero? Repellat, silorem Lorem ipsum
            dolor sit amet
          </p>
          <a href="">Learn more.</a>
        </div>
      </div>
      <div class="footer-bottom">
        <div class="child">
          <h3>WHO ARE WE</h3>
          <ul>
            <li>Our History</li>
            <li>George Soros</li>
            <li>Staff</li>
            <li>Boards</li>
            <li>Policies</li>
            <li>Programs Offices and Foundations</li>
            <li>Financials</li>
          </ul>
        </div>
        <div class="child">
          <h3>HOW WE FUND</h3>
          <ul>
            <li>Our History</li>
            <li>Boards</li>
            <li>Policies</li>
          </ul>
          <div class="child">
            <h3>WHAT WE DO</h3>
            <ul>
              <li>Staff</li>
              <li>Boards</li>
              <li>Policies</li>
            </ul>
          </div>
        </div>
        <div class="child">
          <ul style="padding-top: 2rem">
            <li>Staff</li>
            <li>Boards</li>
            <li>Policies</li>
          </ul>
        </div>
        <div class="child">
          <p style="padding-top: 2rem">
            &copy; 2020 Open Society Foundations, some rights reserved.
          </p>
        </div>
      </div>
      <div class="footer-socials">
        <div class="container">
          <font-awesome-icon icon="user-secret" />
          <i class="fab fa-youtube"></i>
          <font-awesome-icon :icon="['fab', 'fa']" />
        </div>
        <div class="container"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@100;400;700;900&display=swap");
.footer-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  background-color: #020403;
  width: 100%;
  font-family: "Poppins", sans-serif;
}
li {
  list-style: none;
  margin-bottom: 1rem;
  font-size: 0.8rem;
}
.footer {
  width: 70vw;
  color: white;
  justify-content: space-between;
}
.footer .container {
  margin-right: 2rem;
}
.footer h2,
h3 {
  color: #05d192;
}
.footer .container a {
  color: white;
}
.footer-top {
  display: flex;
  flex-wrap: wrap;
  padding: 3rem 0;
}
.footer-top .container {
  flex: 1;
}
.footer-top .container p {
  margin: 1.2rem 0;
}
.footer-bottom {
  display: flex;
  flex-wrap: wrap;
  padding: 2rem 0;
  border-top: 1px solid silver;
  border-bottom: 1px solid silver;
}
.footer-bottom .child {
  flex: 1;
}
.footer-bottom .child h3 {
  margin: 1.2rem 0;
}
.footer ul {
  padding: 0;
}
@media only screen and (max-width: 600px) {
  .footer-top {
    display: block;
    padding: 1rem 0;
  }
  .footer-bottom {
    display: flex;
    padding: 0;
    border-top: 1px solid silver;
    border-bottom: 1px solid silver;
  }
}
</style>