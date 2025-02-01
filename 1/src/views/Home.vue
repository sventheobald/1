<template>
  <div>
    <h1>🏠 Willkommen auf der Startseite!</h1>

    <!-- Kontaktformular nur auf der Startseite -->
    <h2>Kontaktformular</h2>
    <form @submit.prevent="handleSubmit">
      <div>
        <label for="name">Name:</label>
        <input type="text" id="name" v-model="formData.name" required />
      </div>

      <div>
        <label for="email">E-Mail:</label>
        <input type="email" id="email" v-model="formData.email" required />
      </div>

      <div>
        <label for="message">Nachricht:</label>
        <textarea id="message" v-model="formData.message" required></textarea>
      </div>

      <button type="submit">Absenden</button>
    </form>

    <!-- Bestätigung nach Absenden -->
    <div v-if="submitted">
      <h3>Danke für deine Nachricht, {{ formData.name }}!</h3>
      <p><strong>E-Mail:</strong> {{ formData.email }}</p>
      <p><strong>Nachricht:</strong> {{ formData.message }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      formData: {
        name: '',
        email: '',
        message: ''
      },
      submitted: false
    };
  },
  methods: {
    handleSubmit() {
      this.submitted = true;
      console.log("Formulardaten:", this.formData);
    }
  }
};
</script>

<style scoped>
/* Einfaches Styling */
form {
  max-width: 400px;
  margin: 20px auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 8px;
  background-color: #f9f9f9;
}

form div {
  margin-bottom: 15px;
}

label {
  display: block;
  font-weight: bold;
  margin-bottom: 5px;
}

input,
textarea {
  width: 100%;
  padding: 8px;
  box-sizing: border-box;
}

button {
  padding: 10px 20px;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #0056b3;
}

h3 {
  color: green;
}
</style>