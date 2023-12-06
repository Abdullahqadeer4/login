<!-- SignUp.vue -->
<template>
  <div class="signup-container d-flex justify-content-center">
    <form @submit.prevent="handleSubmit">
      <h2>Sign Up</h2>
      <div class="form-group">
        <label for="email">Email:</label>
        <input type="email" id="email" v-model="email" required />
      </div>

      <div class="form-group mt-2">
        <label for="password" >Password:</label>
        <input type="password" id="password" v-model="password" required />
      </div>

      <button type="submit">Sign Up</button>

      <div class="social-buttons">
        <button @click="handleGoogleSignUp">Sign Up with Google</button>
        <button @click="handleFacebookSignUp">Sign Up with Facebook</button>
        <button @click="handleAppleSignUp">Sign Up with Apple</button>
      </div>
    </form>
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
    handleSubmit() {
      // Your form submission logic here
      console.log('Form submitted with:', this.email, this.password);
    },
    handleGoogleSignUp() {
      // Implement Google sign-up logic
      console.log('Signing up with Google');
    },
    handleFacebookSignUp() {
      // Implement Facebook sign-up logic
      console.log('Signing up with Facebook');
    },
    handleAppleSignUp() {
      // Implement Apple sign-up logic
      console.log('Signing up with Apple');
    },
  },
};
</script>

<style lang="scss">
// Improved styling using Sass
.signup-container {
  max-width: 400px;
  margin: 50px auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  text-align: center;

  h2 {
    color: #333;
    margin-bottom: 20px;
  }

  .form-group {
    text-align: left;

    label {
      display: block;
      margin-bottom: 5px;
      color: #333;
    }

    input {
      width: 100%;
      padding: 8px;
      margin-top: 5px;
      box-sizing: border-box;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
  }

  button {
    width: 100%;
    padding: 10px;
    margin-top: 20px;
    background-color: #007bff;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }

  .social-buttons {
    margin-top: 20px;

    button {
      width: 100%;
      padding: 10px;
      margin-top: 10px;
      background-color: #333;
      color: #fff;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
  }
}
</style>
