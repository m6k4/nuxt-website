<template>
  <div class="ContactForm">
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
  justify-content: center;
  align-items: center;
  height: 100%;
}

.ContactForm__form {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
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
  width: 100%;
  padding: 0.5rem;
  border: 1px solid #ccc;
  border-radius: 4px;
  font-size: 1rem;
  outline: none;
  resize: none;
}

.ContactForm__form-label textarea {
  height: 10rem;
}

.ContactForm__form button {
  width: 40%;
  padding: 0.5rem;
  border: 1px solid #2a2a2a;
  border-radius: 4px;
  font-size: 1rem;
  background-color: #2a2a2a;
  color: #ccc;
  cursor: pointer;
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

.success-message {
  margin-top: 1rem;
  color: #2a2a2a;
}

</style>
