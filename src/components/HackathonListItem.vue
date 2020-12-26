<script>
export default {
  props: {
    hackathon: {
      type: Object,
      required: true,
    }
  },
}
</script>

<template>
  <div class="hackathon-list-item">
    <div class="hackathon-list-item__detail">
      <img src="https://kodilan.ams3.digitaloceanspaces.com/companies/superpeer.png" class="hackathon-list-item__logo" />
      <div class="hackathon-list-item__detail-content">
        <span class="hackathon-list-item__detail-content-title">
          {{ hackathon.title }}
        </span>
        <span class="hackathon-list-item__detail-content-description">
          {{ hackathon.description }}
        </span>
      </div>
    </div>
    <span class="hackathon-list-item__detail-date">
      Nov. 27, 2020
    </span>
  </div>
</template>

<style lang="scss">
$border-color: rgb(229,231,235);
$sub-text: rgb(107,114,128);

.hackathon-list-item {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1rem;
  max-width: 720px;
  width: 100%;
  border-bottom: 1px solid $border-color;
  cursor: pointer;

  &__logo {
    width: 80px;
    height: 80px;
  }

  &__detail {
    display: flex;
    align-items: center;

    &-content {
      margin-left: 2rem;
      display: flex;
      flex-direction: column;

      &-title, &-description {
        display: -webkit-box;
        -webkit-box-orient: vertical;
        overflow: hidden;
      }

      &-title {
        font-size: 18px;
        font-weight: 500;
        margin-bottom: 4px;
        -webkit-line-clamp: 1;
      }

      &-description {
        color: $sub-text;
        font-size: 14px;
        -webkit-line-clamp: 2;
      }
    }

    &-date {
      white-space: pre;
    }
  }
}
</style>
