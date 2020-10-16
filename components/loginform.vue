<template>
  <div class="loginform">
    <form v-on:submit.prevent="doLogin" id="form">
      <label for="username">Username</label>
      <input
        id="username"
        v-model="user.username"
        type="text"
        placeholder="Username"
      />

      <label for="password">Password</label>
      <input
        id="password"
        v-model="user.password"
        type="password"
        placeholder="Password"
      />
      <button type="submit">Log In</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      user: {
        username: null,
        password: null,
      },
    };
  },
  methods: {
    doLogin: function () {
      this.submitData = this.user;
    },
  },
};
</script>

<style scoped>
.login-form {
  height: 20vh;
}
</style>