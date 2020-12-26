<script>
import Navbar from "@/components/Navbar";
import Header from "@/components/Header";
import HackathonList from "@/components/HackathonList";
import FAQ from "@/components/FAQ";

export default {
  components: {
    Navbar,
    Header,
    HackathonList,
    FAQ,
  }
};
</script>

<template>
  <div class="home">
    <Navbar />
    <Header />
    <Hackathon-List />
    <FAQ />
  </div>
</template>

<style lang="scss">
.home {
  max-width: 1280px;
  width: 100%;
  margin: 0 auto;
  padding: 2rem;
}
</style>
