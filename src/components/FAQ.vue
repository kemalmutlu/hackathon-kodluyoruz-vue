<script>
import Vue from 'vue';
import { AccordionMenu } from 'vue-accordion-menu';

Vue.component('AccordionMenu', AccordionMenu);

export default {
  data() {
    return {
      contents: [
        {
          title: 'Backend gibi herhangi bir teknoloji kullanabilir miyim?',
          msg: 'Evet. Her bir takım için backend veya herhangi bir teknoloji kullanmaları tamamen serbest olup puanlamada ek olarak avantaj sağlayacağından emin olabilirsiniz. Fakat backend veya web frameworklerinin olmaması takımınızı bu etkinlikte elemez.',
        },
        {
          title: 'Siteye yukarıda belirtilmeyen fakat eklenmesi gerektiğini düşündüğüm bazı detayları ekleyebilir miyim?',
          msg: 'Tabii ki. Kodluyoruz Hackathon tamamen yeni fikirlere ve ayrıcalıklara özen gösteren ve herkesin aklında olanları kodlara dökmek için tamamen serbest olduğu bir etkinliktir.',
        },
      ]
    };
  },
}
</script>

<template>
  <div class="faq_list">
    <h1>Sık sorulan sorular</h1>
    <AccordionMenu :contents="contents"></AccordionMenu>
  </div>
</template>

<style lang="scss">
.faq_list{
  h1{
    text-align: center;
    margin-top: 2em;
  }
  .faq-description{
    .faq-number{
      display: none;
    }
  }

}
</style>
