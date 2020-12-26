<script>
export default {
  data() {
    return {
      firstQuestion: false,
      secondQuestion: false,
    };
  },
}
</script>

<template>
  <section class="accordions">
    <article class="accordion" @click="firstQuestion = !firstQuestion">
      <p>Backend gibi herhangi bir teknoloji kullanabilir miyim?</p>
        <div v-if="firstQuestion" class="accordion-body">
          Evet. Her bir takım için backend veya herhangi bir teknoloji kullanmaları tamamen serbest olup puanlamada ek olarak avantaj sağlayacağından emin olabilirsiniz. Fakat backend veya web frameworklerinin olmaması takımınızı bu etkinlikte elemez.
        </div>
    </article>
    <article class="accordion" @click="secondQuestion = !secondQuestion">
      <p>Siteye yukarıda belirtilmeyen fakat eklenmesi gerektiğini düşündüğüm bazı detayları ekleyebilir miyim?</p>
      <div v-if="secondQuestion" class="accordion-body">
        Tabii ki. Kodluyoruz Hackathon tamamen yeni fikirlere ve ayrıcalıklara özen gösteren ve herkesin aklında olanları kodlara dökmek için tamamen serbest olduğu bir etkinliktir.
      </div>
    </article>
  </section>
</template>

<style lang="scss">
.accordions {
  display: flex;
  align-items: center;
  flex-direction: column;
  margin-top: 2rem;

  .accordion {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}
</style>
