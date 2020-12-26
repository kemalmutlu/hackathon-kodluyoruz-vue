<script>
import Navbar from "../components/Navbar";
import ContentLoader from "../components/ContentLoader";
import Kemal from "../assets/kemal.jpeg";
import Sezer from "../assets/sezer.jpg";
import Cengiz from "../assets/cengiz.jpg";
import Ferhat from "../assets/ferhat.jpg";

export default {
  props: {
    member : {
      type: Object,
      required: true,
    }
  },
  data() {
    return {
      isLoading: false,
      members: [
        {
          name: "Kemal Mutlu",
          title: "Back-End Developer",
          img: Kemal,
          desc: `Moscow is the capital and most populous city of Russia, with 13.2 million residents within the city limits and 17.8 million within the urban area. Moscow has the status of a Russian federal city.`,
        },
        {
          name: "Sezer İstif",
          title: "Software Engineer",
          img: Sezer,
          desc: `Paris is the capital and most populous city of France. By the 17th century, Paris was one of Europe's major centres of finance, commerce, fashion, science, and the arts, and it retains that position still today.`,
        },
        {
          name: "Cengiz C. Mataracı",
          title: "Full Stack Developer",
          img: Cengiz,
          desc: `Rome's history spans more than 2,500 years. While Roman mythology dates the founding of Rome at around 753 BC, the site has been inhabited for much longer, making it one of the oldest continuously occupied sites in Europe.`,
        },
        {
          name: "Ferhat Demir",
          title: "Front-End Developer",
          img: Ferhat,
          desc: `By the end of the 12th century, Paris had become the political, economic, religious, and cultural capital of France. Maurice de Sully undertook the construction of the Notre Dame Cathedral at its eastern extremity.`,
        },
      ],
    };
  },
  components: {
    Navbar,
    ContentLoader,
  },
  activated() {
    this.isLoading = true;
  },
  created() {
    this.isLoading = true;

    setTimeout(() => {
      this.isLoading = false;
    }, 2000);
  },
};
</script>

<template>
  <div class="hackathon-detail-wrapper">
    <Navbar />
    <div class="hackathon-detail">
      <content-loader v-if="isLoading" />
      <template v-else>
        <div class="hackathon-detail__header">
          <!-- <img
            src="https://kodilan.ams3.digitaloceanspaces.com/companies/superpeer.png"
            class="hackathon-detail__header-logo"
          />
          <h1 class="hackathon-detail__header-title">
            Kemal Mutlu
          </h1>
          <! <p class="hackathon-detail__header-date">
            Nov. 27, 2020
          </p> -->
          <!-- </div> -->
          <!-- <div class="hackathon-detail__content"> -->
          <!-- <p> -->
          <!-- Yazılım Mühendisi. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quas, officiis non inventore, ullam aperiam libero debitis recusandae ratione neque sit dolorum ex perferendis dicta vero similique architecto! Placeat, unde velit. Lorem ipsum dolor sit amet consectetur adipisicing elit. Sint id quam blanditiis eaque soluta quibusdam nobis facere dolor esse. Sint qui odit unde possimus quisquam placeat ea, vel incidunt repellat? -->
          <!-- </p> -->
          <div class="location-contain">
            <div
              class="locations"
              v-for="member in members"
              :key="member.name"
            >
              <place :member="member">
                <!-- <h2>{{ member.img }}</h2> -->
                <img :src="member.img" style="width: 220px; height: 280px; border-radius: 50px; box-shadow: 2px 2px black;" />
                <h2>{{ member.name }}</h2>
                <h3>{{ member.title }}</h3>
                <h2>{{ member.desc }}</h2>
              </place>
            </div>
          </div>
        </div>
      </template>
    </div>
  </div>
</template>

<style lang="scss">
$bg-color: rgb(249, 250, 251);
$content-color: rgb(75, 85, 99);
$box-shadow: 0 0.5em 1em -0.125em rgba(10, 10, 10, 0.1),
  0 0 0 1px rgba(10, 10, 10, 0.02);

.hackathon-detail-wrapper {
  max-width: 1280px;
  width: 100%;
  margin: 0 auto;
  padding: 2rem;

  .hackathon-detail {
    margin: 3rem 0;
    border-radius: 8px;
    text-align: center;
    padding: 1rem 4rem;
    box-shadow: $box-shadow;

    &__header {
      &-logo {
        width: 120px;
        height: 120px;
      }

      &-title {
        margin: 0;
      }

      &-date {
        margin: 1rem 2rem 0 0;
      }
    }

    &__content {
      white-space: pre-line;
      color: $content-color;
      line-height: 1.75rem;
      padding-bottom: 2rem;
    }
  }
}
.location-contain {
  display: flex;
  justify-content: center;
}

.place {
  display: flex;
  flex-direction: column;
  width: 280px;
  height: 320px;
  justify-content: center;
  background: white;
  border: 1px solid #ddd;
  padding: 20px 20px;
  margin: 10px;
  h2 {
    margin: 0;
    text-align: center;
  }
  img {
    margin: 10px;
    align-self: center;
  }
}
</style>
