<template>
  <div class="creditCard">
    <input type="text" name="name" id="" placeholder="FullName" />
    <input type="email" name="" id="" placeholder="Email" />
    <input type="password" name="" id="" placeholder="Password" />
    <div>
      <input type="checkbox" name="" id="anonymously" />
      <label for="anonymously"><i>Dontate anonymously</i></label>
    </div>
    <input type="number" placeholder="Card Number" />
    <input type="date" id="" />
    <input type="number" placeholder="Code" id="" />
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.creditCard {
  display: flex;
  flex-direction: column;
}
.creditCard input {
  padding: 10px;
  margin-top: 1rem;
  border-radius: 5px;
  border: none;
}
</style>