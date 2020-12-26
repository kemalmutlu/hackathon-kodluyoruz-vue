<script>
import Navbar from "../components/Navbar";
import ContentLoader from "../components/ContentLoader";

export default {
  data() {
    return {
      isLoading: false,
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
          <img
            src="https://kodilan.ams3.digitaloceanspaces.com/companies/superpeer.png"
            class="hackathon-detail__header-logo"
          />
          <h1 class="hackathon-detail__header-title">
            Software Engineer
          </h1>
          <p class="hackathon-detail__header-date">
            Nov. 27, 2020
          </p>
        </div>
        <div class="hackathon-detail__content">
          <p>
            Farm Vision Technologies is an early-stage startup company focused
            on leveraging computer vision technology to provide growers of
            specialty crops with reliable, accurate, actionable information
            about their groves and orchards. We are a small team, tightly
            focused on developing a proof-of-concept product that excites our
            customers. We are seeking a Senior Data Scientist to take the lead
            in converting the visual metrics we can measure into actionable
            insights for our customers. You will help fruit growers solve
            important problems in their orchards! This is a multidisciplinary
            role containing elements of statistical analysis, agronomy, and
            machine learning.
          </p>
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
</style>
