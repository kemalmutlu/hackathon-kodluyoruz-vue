<template>
  <div class="sponsor">
    <h2 class="h1">Sponsorlar</h2>
    <div class="row">
      <img src="../assets/Sponsors/kablosuzbeyin_500x.png" class="card-img-top kablosuz-beyin" alt="Kablosuz Beyin">
      <img src="../assets/kodluyoruz-logo.png" class="card-img-top" alt="Kodluyoruz">
      <img src="../assets/Sponsors/robotsan.png" class="card-img-top" alt="Robotsan">
    </div>
  </div>
</template>

<style lang="scss">
.sponsor {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-top: 24px;

  .row {
    display: flex;
    align-items: center;
    justify-content: center;

    img {
      width: 18%;
      margin: 0 24px;

      &:first-child {
        width: 10%;
      }
    }
  }
}
</style>
