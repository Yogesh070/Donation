<template>
  <div class="transaction">
    <!-- <h1>{{ topic }} is title</h1> -->
    <div class="checkout">
      <div class="image-container">
        <img
          src="https://www.nepaltrust.org/wp-content/uploads/2019/02/health-picture.jpg"
          alt=""
        />
      </div>
      <div class="amountContainer">
        <div class="amount-input">
          <div>
            <h3>Donate:</h3>
            <ToggleButton />
          </div>

          <div class="amount-box">
            <input
              type="text"
              id="amount"
              v-model="amount"
              @keypress="isNumberKey(e)"
            />
          </div>
        </div>
        <div class="globalGiving">
          <label for="global-giving"
            >Add an optional donation to GlobalGiving to amplify my
            impact:</label
          >
          <select name="global-giving" id="global-giving" v-bind="amount">
            <option value="25percent">$ {{ globalGiving(25) }} (25%)</option>
            <option value="20percent">$ {{ globalGiving(20) }} (20%)</option>
            <option value="15percent">$ {{ globalGiving(15) }} (15%)</option>
            <option value="10percent">$ {{ globalGiving(10) }} (10%)</option>
            <option value="none">I donot wish to amplify my impact</option>
          </select>
        </div>
        <div class="total">
          <h3>Total</h3>
          <h1>${{ amount }}</h1>
        </div>
      </div>
    </div>
    <div class="credit-card">
      <h1>Donate to Healthcare & Opportunity in the Hidden Himalayas</h1>
      <p>and we'll send you updates from The Nepal Trust about your impact!</p>
      <CreditCard />
    </div>
  </div>
</template>

<script>
import ToggleButton from "../components/ToggleButton";
import CreditCard from "../components/CreditCard";
export default {
  components: {
    ToggleButton,
    CreditCard,
  },
  // props: {
  //   topic: String,
  // },
  data() {
    return {
      amount: "",
    };
  },
  methods: {
    globalGiving(n) {
      return ((n / 100) * this.amount).toFixed(1);
    },
    isNumberKey(evt) {
      var charCode = evt.which ? evt.which : event.keyCode;
      return !(charCode > 31 && (charCode < 48 || charCode > 57));
    },
  },
};
</script>

<style scoped>
.transaction {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  /* width: 60vw; */
  /* margin: 0 auto; */
  background-color: #e2e2e2;
}
.checkout {
  background-color: white;
  height: 700px;
  width: 600px;
  padding: 2rem;
}
.image-container {
  position: relative;
}
.image-container img {
  width: 100%;
  height: 100%;
}
.image-container::after {
  content: "Healthcare & Opportunity in the Hidden Himalayas";
  position: absolute;
  bottom: 0;
  left: 0;
  background: rebeccapurple;
  padding: 1rem;
  width: 100%;
  font-weight: 900;
  color: white;
  font-size: 1.2rem;
  opacity: 0.6;
}
.amountContainer {
  margin: 2rem 0;
}
.amount-input {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
#amount {
  width: 80px;
  padding-left: 1.5rem;
  height: 2rem;
}
.amount-input label {
  font-size: 1.5rem;
}
.amount-box {
  position: relative;
}
.amount-box::before {
  content: "$";
  position: absolute;
  top: 5px;
  left: 10px;
  font-weight: 700;
}
.globalGiving {
  border-top: 1px solid slategrey;
  border-bottom: 1px solid slategrey;
  padding: 2rem 0;
  margin: 2rem 0;
}
.total {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
}
.total h3 {
  font-weight: 900;
  font-size: 1.8rem;
}
.credit-card {
  padding: 0 2rem;
}
@media only screen and (max-width: 900px) {
  .transaction {
    flex-wrap: wrap;
  }
}
</style>