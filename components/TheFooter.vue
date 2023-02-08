<template>
  <div class="TheFooter">
    <div class="TheFooter__name">
    <p>Architekt Łukasz Kowalski</p>
  </div>
  <div>
    <p>NAVY 2023</p>
  </div>
</div>
</template>

<script>
export default {
  name: 'TheFooter'
}
</script>
<style lang="css" scoped>
.TheFooter {
    color: #8e8e8e;
    font-size: 0.8rem;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    line-height: 1.5rem;
    padding: 0 10%;
    position: sticky;
    bottom: 0;
  }
.TheFooter__name {
  text-transform: uppercase;
}
</style>
