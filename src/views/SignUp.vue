<template>
  <div class="container1">
    <div class="left-section1 box-page">
      <div class="box">
        <h1 style="text-transform: uppercase">Why register to philsys</h1>
        <p style="text-align: justify">
          As a digital foundational ID system, PhilSys will transform how
          services are delivered and accessed in the Philippines, and accelerate
          our transition to a digital economy, including to enable presenceless,
          paperless and cashless transactions. Built on a Privacy-by-Design
          principle, PhilSys adopts the latest technology and innovations
          underscoring the importance of privacy of individuals and security of
          information under the system.
        </p>
      </div>
    </div>

    <div class="right-section1 signup-page">
      <form class="signup-form" @submit.prevent="handleSubmit">
        <div class="line">
          <div class="input-group">
            <label>First Name:</label>
            <input type="firstname" required v-model="firstname" />
          </div>
          <div class="input-group">
            <label>Middle Name:</label>
            <input type="middlename" required v-model="middlename" />
          </div>
          <div class="input-group">
            <label>Last Name:</label>
            <input type="lastname" required v-model="lastname" />
          </div>
          <div class="input-group">
            <label>Suffix:</label>
            <select v-model="suffix">
              <option value="">-</option>
              <option value="jr">Jr.</option>
              <option value="sr">Sr.</option>
              <option value="i">I</option>
              <option value="ii">II</option>
              <option value="iii">III</option>
              <option value="iv">IV</option>
            </select>
          </div>
        </div>

        <div class="line">
          <div class="input-group">
            <label>Contact Number:</label>
            <input type="contact" required v-model="contact" />
          </div>
          <div class="input-group">
            <label>Date of Birth</label>
            <input type="date" required v-model="birth" />
          </div>
          <div class="input-group">
            <label>Age:</label>
            <input type="number" required v-model="age" />
          </div>
          <div class="input-group">
            <label>Gender:</label>
            <select required v-model="gender">
              <option value="male">Male</option>
              <option value="female">Female</option>
              <option value="other">Other</option>
            </select>
          </div>
        </div>

        <div class="line1">
          <div class="input-group1">
            <label>Email:</label>
            <input type="email" required v-model="email" />
          </div>
          <div class="input-group1">
            <label>Password:</label>
            <input type="password" required v-model="password" />
            <div v-if="passwordError" class="error">{{ passwordError }}</div>
          </div>
        </div>

        <div class="terms">
          <input type="checkbox" required v-model="terms" />
          <label>Accept Terms and Conditions</label>
        </div>

        <div class="submit">
          <button class="signup-button1">Sign Up</button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      firstname: "",
      middlename: "",
      lastname: "",
      suffix: "",
      contact: "",
      birth: "",
      age: "",
      gender: null,
      email: "",
      password: "",
      terms: false,
      passwordError: "",
    };
  },
  methods: {
    handleSubmit() {
      this.passwordError =
        this.password.length > 7
          ? ""
          : "Password must be at least 8 characters long";

      if (!this.passwordError) {
        console.log("Form Submitted!");
        console.log("first name: ", this.firstname);
        console.log("middle name: ", this.middlename);
        console.log("last name: ", this.lastname);
        console.log("suffix: ", this.suffix);
        console.log("contact number: ", this.contact);
        console.log("date of birth: ", this.birth);
        console.log("age: ", this.age);
        console.log("gender: ", this.gender);
        console.log("email: ", this.email);
        console.log("password: ", this.password);
        console.log("terms: ", this.terms);

        this.firstname = "";
        this.lastname = "";
        this.middlename = "";
        this.suffix = "";
        this.contact = "";
        this.birth = "";
        this.age = "";
        this.gender = "";
        this.email = "";
        this.password = "";
        this.terms = "";
      }
    },
  },
};
</script>

<style>
body {
  padding-top: 150px;
}

.container1 {
  display: flex;
  padding: 20px;
}

.left-section1 {
  flex: 1;
}

.box-page {
  margin-top: 35px;
}

.box {
  background-color: #134087;
  color: white;
  padding: 20px;
  margin-right: 20px;
  font-size: 0.9em;
  text-align: left;
  letter-spacing: 1.5px;
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
  font-family: Arial, sans-serif;
}

.right-section1 {
  flex: 2;
}

.signup-page {
  margin-top: -35px;
}

.signup-form {
  max-width: 1000px;
  margin: 0 auto;
  margin-top: 0px;
  background: white;
  text-align: left;
  padding: 40px;
  border-radius: 10px;
  font-family: Arial, sans-serif;
}

.line {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}

.input-group {
  width: calc(25% - 10px);
}

.line1 {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}

.input-group1 {
  width: calc(50% - 10px);
}

label {
  color: #333;
  display: inline-block;
  margin: 25px 0 15px;
  font-size: 0.7em;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: bold;
  font-family: Arial, sans-serif;
}

input,
select {
  display: block;
  padding: 10px 2px;
  width: 100%;
  box-sizing: border-box;
  border: 1px solid #ddd;
  border-radius: 5px;
  color: #555;
  font-family: Arial, sans-serif;
}

input[type="checkbox"] {
  display: inline-block;
  width: 16px;
  margin: 0 10px 0 0;
  position: relative;
  top: 2px;
}

.error {
  color: #e44343;
  margin-top: 10px;
  font-size: 0.8em;
  font-weight: bold;
}

.signup-button1 {
  background: #fdc910;
  border: 0;
  padding: 10px 20px;
  margin-top: 20px;
  margin-bottom: 20px;
  color: white;
  text-transform: uppercase;
  border-radius: 20px;
  display: block;
  margin: 0 auto;
  font-weight: bold;
}
</style>