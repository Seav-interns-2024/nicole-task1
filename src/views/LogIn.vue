<template>
  <div class="container">
    <div class="left-section">
      <img src="@/assets/chart.png" class="chart" alt="chart">
      <p style="font-size: 0.9em; color: #293e71; font-style: italic;">Registration as of March 15, 2024</p>
    </div>
    <div class="right-section">
      <form class="login-form">
        <label>Email:</label>
        <input type="email" required v-model="email" />

        <label>Password:</label>
        <input type="password" required v-model="password" style="margin-bottom: 20px" />
        
        <div class="submit">
          <button class="login-button">Log In</button>
        </div>
      </form>

      <div class="signup">
        <p style="font-size: 0.9em">
          Don't have an account yet?
          <button class="signup-button" @click="goToSignUp">Sign Up</button>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: '',
      password: '',
    };
  },
  methods: {
    goToSignUp() {
      this.$router.push("/signup");
    },
  },
};
</script>

<style scoped>
body {
  padding-top: 150px;
}

.container {
  display: flex;
  padding: 30px;
}

.left-section {
  flex: 2;
}

.right-section {
  flex: 2;
}

.login-form {
  max-width: 420px;
  margin: 0 auto;
  background: white;
  text-align: left;
  padding: 40px;
  border-radius: 10px;
  font-family: Arial, sans-serif;
}

label {
  color: #333;
  display: inline-block;
  margin: 25px 0 15px;
  font-size: 0.7em;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: bold;
}

input {
  display: block;
  padding: 10px 6px;
  width: 100%;
  box-sizing: border-box;
  border: 1px solid #ddd;
  border-radius: 5px;
  color: #000000;
  font-family: Arial, sans-serif;
}

.login-button {
  background: #fdc910;
  border: 0;
  padding: 10px 20px;
  margin-top: px;
  margin-bottom: 20px;
  color: white;
  text-transform: uppercase;
  border-radius: 20px;
  display: block;
  margin: 0 auto;
  font-weight: bold;
}

.signup-button {
  background: none;
  border: 0;
  font-weight: bold;
  color: #134087;
  cursor: pointer;
}

.signup p {
  margin-top: 20px;
  text-align: center;
}

.chart {
  width: 600px;
  height: auto;
}
</style>
