<script>
import HackathonListItem from './HackathonListItem';

export default {
  components: {
    HackathonListItem
  },
  data() {
    return {
      hackathons: [
        {
        title: 'Senior Data Scientist',
        description: 'Lorem ipsum dolor sit.',
        id: Math.random() * 7,
        },
        {
        title: 'Software Engineer',
        description: 'Lorem ipsum dolor sit Lorem ipsum dolor sit Lorem ipsum dolor sit Lorem ipsum dolor sit Lorem ipsum dolor sit Lorem ipsum dolor sit Lorem ipsum dolor sit Lorem ipsum dolor sit Lorem ipsum dolor sit Lorem ipsum dolor sit Lorem ipsum dolor sit Lorem ipsum dolor sit',
        id: Math.random() * 7,
        },
        {
        title: 'Machine Learning Engineer',
        description: 'Lorem ipsum dolor sit.',
        id: Math.random() * 7,
        }
      ]
    };
  },
  methods: {
    redirectToDetailPage() {
      this.$router.push({ name: 'HackathonDetail' });
    }
  },
}
</script>

<template>
  <div class="hackathon-list">
    <h1 class="hackathon-list__title">10 Open Remote Machine Learning Jobs</h1>
    <hackathon-list-item
          v-for="hackathon in hackathons"
          :key="hackathon.id"
          :hackathon="hackathon"
          @click.native="redirectToDetailPage"
    />
  </div>
</template>

<style lang="scss">
.hackathon-list {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 2rem;
}
</style>
