<template>
  <div class="AddressInfo">
    <div class="AddressInfo__address">
      <div class="AddressInfo__address-title">
        <div class="main-title">
          Dane firmy:
        </div>
        <div class="subtitle">
          NAVY Architekt Łukasz Kowalski
        </div>
      </div>
      <div class="AddressInfo__address-description">
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
}

.AddressInfo__address {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-top: 2rem;
}

.AddressInfo__address-title {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 1rem;
}

.AddressInfo__address-title .main-title {
  font-size: 1.5rem;
  font-weight: 500;
}

.AddressInfo__address-title .subtitle {
  font-size: 1.2rem;
  font-weight: 400;
}

.AddressInfo__address-description {
  margin-top: 1.5rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.AddressInfo__address-description p {
  font-size: 1rem;
  font-weight: 400;
  margin: 0.5rem 0;
}
</style>
