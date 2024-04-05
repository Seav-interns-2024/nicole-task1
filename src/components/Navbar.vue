<template>
  <nav class="navbar">
    <div class="container">
      <div class="navbar-content">
        <div class="logo-container">
          <img src="@/assets/logo1.png" class="logo" alt="logo1">
          <img src="@/assets/logo2.png" class="logo logo2" alt="logo2">
          <div class="company-name">
            <span>Philippine</span>
            <span>Identification</span>
            <span>System</span>
          </div>
        </div>
        <ul class="navbar-menu">
          <li><a href="#">Home</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Registration</a></li>
          <li><a href="#">Use Cases</a></li>
          <li><a href="#">ePhilID</a></li>
          <li><a href="#">News and Events</a></li>
          <li><a href="#">Testimonials</a></li>
          <li><a href="#">Contact Us</a></li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navbar'
};
</script>

<style>
/* Your existing styles */

.navbar {
  background-color: #294278;
  color: white;
  position: fixed;
  width: 100%;
  top: 0;
  left: 0;
  z-index: 1000;
  border-bottom: 1px solid #dddddd;
}

.container {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 10px 25px;
}

.navbar-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}

.logo-container {
  display: flex;
  align-items: center;
}

.navbar-menu {
  list-style-type: none;
  margin: 0;
  padding: 0;
  display: flex;
  font-size: 0.95em;
}

.navbar-menu li {
  margin-right: 50px; /* Adjust spacing between navigation items */
}

.navbar-menu li:last-child {
  margin-right: 0; /* Remove margin from last navigation item */
}

.navbar-menu li a {
  color: white;
  text-decoration: none;
  text-transform: uppercase; /* Convert text to uppercase */
  font-weight: bold; /* Apply bold font weight */
}

.logo {
  width: 90px;
  height: auto;
  margin-right: 10px; /* Add margin between logo1 and logo2 */
}

.company-name {
  text-transform: uppercase;
  text-align: left;
  display: flex;
  flex-direction: column;
  white-space: nowrap;
  margin-left: 20px;
}

.company-name span {
  font-size: 1.2em;
}
</style>
