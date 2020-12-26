<script>
export default {
  methods: {
    redirectToDiscord() {
      window.open(`https://discord.gg/fBGEkpGrB5`);
    }
  },
}
</script>

<template>
  <div class="navbar">
    <div class="navbar__link">
      <router-link to="/">
        <img src="https://cdn.sanity.io/images/9kdepi1d/production/65c832d202a503b15d99e628f4313782f3ef50db-300x62.png" alt="Kodluyoruz logo">
      </router-link>
      <a href="">
        Home
      </a>
      <a href="">
        About
      </a>
      <a href="">
        Find a machine learning mentor
      </a>
    </div>
    <div class="navbar__discord-link">
      <button @click="redirectToDiscord">
        Discord
      </button>
    </div>
  </div>
</template>

<style lang="scss">
$link-color: rgb(107,114,128);
$link-hover-color: rgb(22,30,46);


.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;

  &__link {
    display: flex;
    align-items: center;

    img {
      height: 40px;
    }

    a {
      text-decoration: none;
      margin-left: 1.75rem;
      margin-right: 1.75rem;
      color: $link-color;
      font-weight: 500;

      &:hover {
        transition: .3s;
        color: $link-hover-color;
      }
    }
  }

  &__discord-link {
    button {
      padding: 1rem 2rem;
      border-radius: 6px;
      background-color: #7289DA;
      color: #FFF;
      border: none;
      cursor: pointer;

      &:focus {
        outline: none;
      }
    }
  }
}
</style>
