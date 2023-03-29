<template>
  <div class="AddressInfo">
    <div class="AddressInfo__address">
      <div class="AddressInfo__address-title">
          Dane kontaktowe:
      </div>
      <div class="AddressInfo__address-description">
        <p>NAVY Architekt Łukasz Kowalski</p>
        <p>ul. Konstruktorska 10C/31</p>
        <p>02-673 Warszawa</p>
        <p>NIP 5423106116 REGON 383147338</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AddressInfo'

}
</script>

<style lang="css" scoped>

.AddressInfo {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 2rem 0;
  text-transform: none;
  margin-bottom: 5rem
}

.AddressInfo__address {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.AddressInfo__address-title {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  font-size: 1rem;
  font-weight: 500;
}

.AddressInfo__address-title .subtitle {
  font-size: 0.9rem;
}

.AddressInfo__address-description {
  margin-top: 1.5rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.AddressInfo__address-description p {
  font-size: 0.9rem;
  font-weight: 400;
  margin: 0;
}
@media only screen and (max-width: 1150px) {
  .AddressInfo {
    margin-bottom: 2rem
  }
}
</style>
