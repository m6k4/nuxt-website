<template>
  <div class="ContactInfo">
    <div class="ContactInfo__description">
      Chętnie odpowiem na każde pytanie, zapraszam do kontaktu za pośrednictwem formularza dostępnego poniżej.
    </div>
    <div class="ContactInfo__description">
      Wszystkich zainteresowanych usługami projektowymi Studia NAVY zapraszam na bezpłatne spotkanie, podczas którego porozmawiamy o Państwa wymaganiach i oczekiwaniach. Spotkanie takie ma charakter niezobowiązującej prezentacji – wierzę, że pomoże Państwu w ewentualnym podjęciu decyzji o współpracy z NAVY.
    </div>
    <div class="ContactInfo__contact-details">
      <div class="contact">
        <span> tel: 666 060 169 </span>
        <span> mail: kontakt@navy.com.pl </span>
      </div>
      <div class="socials">
        <a href="tel:+48666060169" title target="_self" class="phone">
          <nuxt-img
            :lazy="true"
            format="webp"
            :src="phone"
            alt="phone icon"
          />
        </a>
        <a href="mailto:kontakt@navy.com.pl" title="" target="_self" class="email">
          <nuxt-img
            :lazy="true"
            format="webp"
            :src="email"
            alt="email icon"
          />
        </a>
        <a href="http://facebook.com/navyinteriors" title="" target=" _blank" class="facebook">
          <nuxt-img
            :lazy="true"
            format="webp"
            :src="facebook"
            alt="facebook icon"
          />
        </a>
        <a href="http://instagram.com/navy_interiors" title="" target=" _blank" class="instagram">
          <nuxt-img
            :lazy="true"
            format="webp"
            :src="instagram"
            alt="instagram icon"
          />
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ContactInfo',
  data () {
    return {
      facebook: '/images/facebook.webp',
      instagram: '/images/instagram.webp',
      phone: '/images/phone.webp',
      email: '/images/email.webp'
    }
  }
}
</script>

<style lang="css" scoped>
.ContactInfo {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 2rem 0;
  text-transform: none;
}

@media only screen and (max-width: 1400px) {
  .ContactInfo {
    padding: 2rem 0rem;
  }
}

.ContactInfo__title {
  font-size: 0.9rem;
  font-weight: 500;
  margin-bottom: 2rem;
}

.ContactInfo__description {
  font-size: 0.9rem;
  font-weight: 400;
}

.ContactInfo__contact-details {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-top: 2rem;
  gap: 3rem;
}

.contact {
  display: flex;
  gap: 4rem;
  font-weight: 400;
  font-size: 0.9rem;
}

@media only screen and (max-width: 750px) {
  .contact {
    flex-direction: column;
    gap: 1rem;
    text-align: left;
  }

  .ContactInfo__description {
    text-align: center;
  }
}

.socials {
  width: 100%;
  display: flex;
  justify-content: space-between;
}

.socials:hover {
  cursor: pointer;
}

.socials img{
  height: 1.8rem;
}
</style>
