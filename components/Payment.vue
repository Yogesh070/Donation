<template>
  <div class="payment">
    <h2>Select Donation Amount</h2>
    <div class="amount-box">
      <button
        class="amount-button"
        @click="isActive1 = !isActive1"
        :class="{ active: isActive1 }"
      >
        $10
      </button>
      <button
        class="amount-button"
        @click="isActive2 = !isActive2"
        :class="{ active: isActive2 }"
      >
        $20
      </button>
      <button
        class="amount-button"
        @click="isActive3 = !isActive3"
        :class="{ active: isActive3 }"
      >
        $30
      </button>
      <button
        class="amount-button"
        @click="isActive4 = !isActive4"
        :class="{ active: isActive4 }"
      >
        $40
      </button>
    </div>
    <input type="text" id="" placeholder="Other Amount" />
    <div>
      <button>Donate Online</button>
      <button>Donate Offline</button>
    </div>
    <h3>PAYMENT METHOD</h3>
    <div class="payment-method">
      <div>
        <img
          src="https://cdn.worldvectorlogo.com/logos/paypal.svg"
          alt="paypal"
        />
      </div>
      <div>
        <img
          src="https://cdn.iconscout.com/icon/free/png-512/payment-visa-card-pay-checkout-transaction-bank-51303.png"
          alt="visa"
        />
      </div>
    </div>
    <select name="time" id="time">
      <option value="One time">One Time</option>
      <option value="Monthly">Monthly</option>
      <option value="Weekly">Weekly</option>
      <option value="Yearly">Yearly</option>
    </select>
    <button>Donate Now</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isActive1: false,
      isActive2: false,
      isActive3: false,
      isActive4: false,
    };
  },
  methods: {
    isActive: function () {
      if (this.isActive1 == true) {
        this.isActive2 = false;
        this.isActive3 = false;
        this.isActive4 = false;
      }
    },
  },
};
</script>

<style scoped>
.payment {
  background-color: white;
  position: relative;
  top: 55px;
  margin-right: 50px;
  width: 385px;
  height: 80vh;
  -webkit-box-shadow: 0px 0px 8px 1px rgba(0, 0, 0, 0.55);
  -moz-box-shadow: 0px 0px 8px 1px rgba(0, 0, 0, 0.55);
  box-shadow: 0px 0px 8px 1px rgba(0, 0, 0, 0.55);
  padding: 2rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}
.payment input {
  outline: none;
  border: none;
  font-size: 18px;
  border-bottom: 1px solid silver;
  margin-bottom: 2rem;
  width: 100%;
  text-align: center;
}
button {
  padding: 0.8rem 1.2rem;
  font-size: 0.9rem;
  color: #ffff;
  background-color: #05d192;
  border: none;
  font-weight: 900;
  outline: none;
  cursor: pointer;
  margin: 1rem 0;
}
.amount-box {
  margin: 2rem 0;
}
.amount-button {
  padding: 0.8rem 1.2rem;
  font-size: 0.9rem;
  color: #05d192;
  background-color: white;
  border: 2px solid #05d192;
  font-weight: 900;
  outline: none;
  cursor: pointer;
}
.payment-method {
  display: flex;
}
.payment-method img {
  min-width: 88px;
  max-height: 25px;
  object-fit: contain;
}
.payment-method div {
  border: 2px solid #05d192;
  padding: 10px;
  margin: 1rem;
  cursor: pointer;
}
select {
  margin: 1rem 0;
  padding: 15px;
  font-size: 14px;
  color: #05d192;
  font-weight: 700;
  outline: none;
  border-color: #05d192;
}
.active {
  background-color: #05d192;
  color: white;
}
@media (max-width: 600px) {
  .payment {
    display: none;
  }
}
</style>