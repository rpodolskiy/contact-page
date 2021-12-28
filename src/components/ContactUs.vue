<template>
  <form @submit.prevent="handleSubmit">
    <div class="title">
      <h1>Contact 
        <span>Us</span>
      </h1>
    </div>

    <label>Name:</label>
    <input type="name" required v-model="name">

    <label>Email:</label>
    <input type="email" required v-model="email">

    <label>Message:</label>
    <textarea rows="10" cols="50" required v-model="message"></textarea>

    <div class="submit">
      <button>Submit</button>
    </div>
  </form>
</template>

<script>
export default {
  data() {
    return {
      email: '',
      name: '',
      message: '',
    }
  },
  methods: {
    handleSubmit() {
      console.log('form submited');
      console.log('name ', this.name);
      console.log('email: ', this.email);
      console.log('message ', this.message);
    }
  }
}
</script>

<style>
  form {
    max-width: 420px;
    margin: 30px auto;
    background: #fff;
    text-align: left;
    padding: 40px;
  }

  h1 {
    color: #000;
    line-height: 3rem;
    font-weight: 700;
    font-family: Roboto, sans-serif;
    font-size: 36px;
  }

  span {
    color: #007bff;
    line-height: 3rem;
    font-weight: 700;
    font-family: Roboto, sans-serif;
    font-size: 36px;
  }

  .title {
    text-align: center;
  }

  label {
    font-family: Roboto, sans-serif;
    font-size: 18px;
    color: #000;
    display: inline-block;
    margin: 25px 0 15px;
    letter-spacing: 1px;
    font-weight: bold;
  }

  input {
    display: block;
    padding: 10px 6px;
    width: 100%;
    box-sizing: border-box;
    border: none;
    border-bottom: 1px solid #ddd;
    color: #555;
  }

  input:focus {
    outline: none !important;
    border-color: #007bff;
  }

  textarea {
    padding: 10px;
    max-width: 100%;
    line-height: 1.5;
    border-radius: 5px;
    border: 1px solid #ccc;
  }

  textarea:focus {
    outline: none !important;
    border-color: #007bff;
  }

  button {
    background: #007bff;
    color: #fff;
    width: 170px;
    font-family: Roboto, sans-serif;
    font-size: 18px;
    border: 0;
    border-radius: 10px;
    padding: 10px 20px;
    margin-top: 20px;
    cursor: pointer;    
  }

  button:active {
    background: #fff;
    color: #007bff;
    border: 1px solid #007bff;
  }

  .submit {
    text-align: center;
  }
</style>