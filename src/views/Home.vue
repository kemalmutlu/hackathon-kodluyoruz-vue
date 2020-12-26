<script>
import Navbar from "@/components/Navbar";
import Header from "@/components/Header";
import HackathonList from "@/components/HackathonList";
import Timer from "@/components/Timer";
import FAQ from "@/components/FAQ";
import Sponsor from "@/components/Sponsor";

export default {
  components: {
    Navbar,
    Header,
    HackathonList,
    Timer,
    FAQ,
    Sponsor,
  }
};
</script>

<template>
  <div class="home">
    <Navbar />
    <Header />
    <Timer />
    <Hackathon-List />
    <FAQ />
    <Sponsor />
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
