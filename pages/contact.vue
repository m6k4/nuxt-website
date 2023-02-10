<template>
  <div class="contact">
    <TheContentComponent :title="title" :content="content" :main-image="image" />
    <div class="contact__form">
      <ContactForm class="form-box" />
    </div>
  </div>
</template>
<script>
import TheContentComponent from '~/components/TheContentComponent'
import ContactForm from '~/components/ContactForm'

export default {
  name: 'ContactPage',
  components: {
    TheContentComponent,
    ContactForm
  },
  layout: 'page',
  data () {
    return {
      image: 'images/contact_image.jpg',
      title: 'Kontakt.',
      content: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum. Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old. Richard McClintock, a Latin professor at Hampden-Sydney College in Virginia, looked up one of the more obscure Latin words, consectetur, from a Lorem Ipsum passage, and going through the cites of the word in classical literature, discovered the undoubtable source.'
    }
  }

}
</script>
<style lang="css" scoped>
.contact__form {
  width: 100%;
  padding: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.form-box {
  width: 600px;
}
</style>
