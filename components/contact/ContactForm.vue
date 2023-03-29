<template>
  <div class="ContactForm">
    <div class="ContactForm__title">
      <div class="main-title">
        Skontaktuj się ze mną
      </div>
    </div>
    <form class="ContactForm__form" @submit.prevent="submitForm">
      <label class="ContactForm__form-label">
        <span class="label-title">Adres email</span>
        <input v-model="email" type="email" name="email">
      </label>
      <label class="ContactForm__form-label">
        <span class="label-title">Treść wiadomości</span>
        <textarea v-model="message" name="message" />
      </label>
      <button type="submit" :disabled="isLoading || !email">
        Wyślij
      </button>
      <span v-if="isSuccess" class="success-message">
        Dziękujemy, twoja wiadomość została wysłana.
      </span>
    </form>
  </div>
</template>

<script>
export default {
  name: 'ContactForm',

  data () {
    return {
      email: '',
      message: '',
      endpoint: 'https://formspree.io/f/mrgvplnp',
      isLoading: false,
      isSuccess: false
    }
  },
  methods: {
    async submitForm () {
      const data = {
        email: this.email,
        message: this.message
      }
      try {
        this.isLoading = true
        this.isSuccess = false
        await this.$axios.$post(this.endpoint, data)
        this.isSuccess = true
      } catch (error) {
      }
      this.isLoading = false
    }
  }
}
</script>

<style lang="css" scoped>
.ContactForm {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 5rem 0 2rem;
}

@media only screen and (max-width: 1150px) {
  .ContactForm {
    padding: 0 0 2rem;;
  }
}

.ContactForm__title {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  margin-bottom: 3rem;
}

.ContactForm__title .main-title {
  font-size: 1.1rem;
  font-weight: 500;
}

.ContactForm__title .subtitle {
  font-size: 0.9rem;
  font-weight: 400;
}

.ContactForm__form {
  width: 80%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

@media only screen and (max-width: 1150px) {
  .ContactForm__form {
    width: 100%;
    padding: 0 5rem;
  }
}

.ContactForm__form-label {
  width: 100%;
  display: flex;
  flex-direction: column;
  margin-bottom: 1rem;
}

.ContactForm__form-label .label-title {
  margin-bottom: 0.5rem;
}

.ContactForm__form-label input,
.ContactForm__form-label textarea {
  padding: 0.5rem 1rem;
  font-size: 0.9rem;
  outline: none;
  resize: none;
  border-width: 0;
  outline: 0;
  background-color: #E0E0E0;
}

.ContactForm__form-label textarea {
  height: 10rem;
}

.ContactForm__form button {
  width: 40%;
  padding: 0.5rem;
  border: 1px solid #2a2a2a;
  font-size: 1rem;
  background-color: #2a2a2a;
  color: #ccc;
  cursor: pointer;
  margin-top: 0.5rem
}

.ContactForm__form button:hover {
  border: 1px solid #434343;
  background-color: #434343;
  cursor: pointer;
}

.ContactForm__form button:active {
  border: 1px solid #434343;
  background-color: #434343;
  cursor: pointer;
}

.ContactForm__form button:focus {
  outline: none;
  cursor: pointer;
}

.ContactForm__form button:disabled {
  cursor: auto;
}

.ContactForm__form button:disabled:hover {
  border: 1px solid #2a2a2a;
  background-color: #2a2a2a;
}

@media only screen and (max-width: 750px) {
  .ContactForm__form {
    padding: 0 2rem;
    width: 90%;
  }

  .ContactForm__form button {
    width: 100%;
  }
}
@media only screen and (max-width: 750px) {
  .ContactForm__form {
    padding: 0;
  }
}
.success-message {
  margin-top: 1rem;
  color: #2a2a2a;
}

</style>
