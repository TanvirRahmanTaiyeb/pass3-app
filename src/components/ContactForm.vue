<template>
  <div class="contact">
    <h2>Contact Me</h2>
    <form @submit.prevent="submitForm">
      <div class="form-group">
        <label for="name">Name:</label>
        <input type="text" id="name" v-model="name" required />
      </div>

      <div class="form-group">
        <label for="email">Email:</label>
        <input type="email" id="email" v-model="email" required />
      </div>

      <div class="form-group">
        <label for="message">Message:</label>
        <textarea id="message" v-model="message" required></textarea>
      </div>

      <div class="form-group">
        <label for="areaOfInterest">Area of Interest:</label>
        <ul>
          <li v-for="(interest, index) in areaOfInterest" :key="index">{{ interest }}</li>
        </ul>
        <input type="text" id="areaOfInterest" v-model="newInterest" @keyup.enter="addInterest" />
      </div>

      <button type="submit">Submit</button>
    </form>

    <div class="form-alert" v-if="formSubmitted">
      Your form has been submitted successfully.
    </div>
    
    <div class="form-error" v-if="formError">
      There was an error submitting the form. Please try again later.
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      email: '',
      message: '',
      areaOfInterest: [],
      newInterest: '',
      formSubmitted: false,
      formError: false,
    };
  },
  methods: {
    submitForm() {
      // Simulating a form submission for demonstration purposes
      if (this.name && this.email && this.message) {
        // Form submission successful
        this.formSubmitted = true;
        this.formError = false;
      } else {
        // Form submission failed
        this.formSubmitted = false;
        this.formError = true;
      }
    },
    addInterest() {
      if (this.newInterest.trim() !== '') {
        this.areaOfInterest.push(this.newInterest);
        this.newInterest = '';
      }
    },
  },
};
</script>

<style scoped>
/* Add contact page styles here */
.form-group {
  margin-bottom: 20px;
}

ul {
  list-style: none;
  margin: 0;
  padding: 0;
}

li {
  margin-bottom: 5px;
}

.form-alert {
  margin-top: 10px;
  color: green;
}

.form-error {
  margin-top: 10px;
  color: red;
}
</style>
