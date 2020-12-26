<template>
  <div class="header">
    <div class="header__content">
      <h1 class="header__content-title">Remote Machine Learning Jobs</h1>
      <p class="header__content-description">The number one place to find remote work in Machine Learning, Data Science, Deep Learning and Artificial Intelligence . Get new jobs to your inbox daily.</p>
      <div class="header__content-submit-container">
        <input type="text" placeholder="Enter your email">
        <button>Notify me</button>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
$main-color: rgb(255,138,76);

.header {
  padding: 6rem 2rem;
  border-radius: 32px;
  margin-top: 2rem;
  background-color: $main-color;
  background-image: url(https://remoteml.com/static/img/cubes.png);

  &__content {
    display: flex;
    flex-direction: column;
    align-items: center;
    max-width: 900px;
    width: 100%;
    margin: 0 auto;

    &-title {
      font-size: 4rem;
      color: #FFF;
      font-weight: 800;
      margin-bottom: 0;
    }

    &-description {
      color: #FFF;
      font-size: 20px;
      text-align: center;
      padding: 0 2rem;
    }

    &-submit-container {
      width: 100%;
      display: flex;
      justify-content: center;

      input {
        width: 40%;
      }

      input, button {
        border: none;
        padding: 1.5rem;
        background-color: #FFF;
        border-radius: 6px;
        font-size: 18px;

        &:focus {
          outline: none;
        }
      }

      button {
        margin-left: 0.5rem;
        color: $main-color;
        cursor: pointer;
      }
    }
  }
}
</style>
