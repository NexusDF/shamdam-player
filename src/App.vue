<template>
  <div class="container">
    <v-header>{{ title }}</v-header>
    <main class="wrapper">
      <section class="artist">
        <div class="artist__logo">
          <img class="artist__image" src="./assets/anime.jpg" />
        </div>
        <div class="artist__header">
          <div class="artist__top">
            <span class="artist__who">ИСПОЛНИТЕЛЬ</span>
            <h1 class="artist__name">MC СНЮС</h1>
            <span class="artist__like">Нравится всем</span>
          </div>
          <div class="artist__bottom">
            <v-button color="yellow">
              <VIcon name="play_arrow" size="24" />
              Слушать
            </v-button>
            <v-button>
              <VIcon name="favorite_border" size="24" />
              1488
            </v-button>
            <v-button>
              <VIcon name="share" size="24" />
            </v-button>
            <v-button color="white" class="artist__radio">
              <VIcon name="podcasts" size="24" />
              Радио
            </v-button>
            <v-button color="white">
              <VIcon name="block" size="24" />
            </v-button>
          </div>
        </div>
      </section>
      <div class="menu"></div>
      <section class="list-of-songs">
        <div class="list-top">
          <h2 class="list-top__header">Популярные треки</h2>
          <span class="list-top__see-all">Смотреть все</span>
        </div>
        <div class="list-of-songs__list">
          <ul class="list-of-songs__list-song">
            <li class="list-song">
              <div class="list-song__logo">
                <img
                  class="list-song__image"
                  src="https://al-school.ru/wp-content/uploads/2019/12/Granit-Vit-Portion-Snus-Open.jpg"
                />
              </div>
              <div class="list-song__wrap">
                <div class="list-song__name">
                  <span class="list-song__title">
                    MC Снюс - Снюс is my life
                  </span>
                </div>
                <div class="list-song__buttons">
                  <v-button color="song-darkgrey">
                    <VIcon name="download" size="28" />
                  </v-button>
                  <v-button color="song-darkgrey">
                    <VIcon name="favorite_border" size="28" />
                  </v-button>
                  <span class="list-song__time">4:20</span>
                </div>
              </div>
            </li>
            <li class="list-song">
              <div class="list-song__logo">
                <img
                  class="list-song__image"
                  src="https://al-school.ru/wp-content/uploads/2019/12/Granit-Vit-Portion-Snus-Open.jpg"
                />
              </div>
              <div class="list-song__wrap">
                <div class="list-song__name">
                  <span class="list-song__title">
                    MC Снюс - Снюс is my life
                  </span>
                </div>
                <div class="list-song__buttons">
                  <v-button color="song-darkgrey">
                    <VIcon name="download" size="28" />
                  </v-button>
                  <v-button color="song-darkgrey">
                    <VIcon name="favorite_border" size="28" />
                  </v-button>
                  <span class="list-song__time">4:20</span>
                </div>
              </div>
            </li>
          </ul>
        </div>
      </section>
    </main>
    <VControl />
  </div>
</template>

<script>
import config from "./app.config.js";
import VHeader from "./components/VHeader.vue";
import VControl from "./components/VControl.vue";

export default {
  created() {
    document.title = config.title;
  },
  data() {
    return {
      title: config.title,
    };
  },
  components: {
    VHeader,
    VControl,
  },
};
</script>

<style lang="scss">
@import "./scss/imports";

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background-color: $backgroundColor;
  font-family: "Inter", sans-serif;
  min-height: 100vh;
  width: 100%;
}

.container {
  background-color: $primary;
  min-height: 100vh;
  width: 1140px;
  display: flex;
  margin: 0 auto;
  position: relative;
  flex-direction: column;
}

.wrapper {
  display: flex;
  flex-direction: column;
  padding: 20px;
}

.artist {
  display: flex;

  &__logo {
    width: 200px;
    height: 200px;
    margin-right: 10px;
  }

  &__image {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    object-fit: cover;
  }

  &__header {
    display: flex;
    flex-direction: column;
    width: 100%;
    justify-content: space-between;
    margin-left: 10px;
  }

  &__top {
    width: 100%;
  }

  &__who {
    color: $spanGrey;
  }

  &__name {
    letter-spacing: 0.05em;
    font-size: 45px;
    font-weight: 700;
  }

  &__like {
    color: $spanGrey;
  }

  &__bottom {
    width: 100%;
    display: flex;
    column-gap: 8px;
  }

  &__radio {
    margin-left: auto;
  }
}

.menu {
  margin: 30px 0;
  border-bottom: solid 1px $borderColor;
}

.list-of-songs {
  display: flex;
  flex-direction: column;

  &__list {
    display: flex;
    margin-left: -7px;
  }

  &__list-song {
    list-style-type: none;
    width: 100%;
  }
}

.list-top {
  display: flex;
  margin: 25px 0;
  justify-content: space-between;
  align-items: center;
}

.list-song {
  display: flex;
  align-items: center;
  padding: 7px;
  min-height: 50px;
  height: auto;
  width: auto;
  justify-content: space-between;

  &:hover {
    border: solid 2px $second;
    padding: 5px;
  }

  & + & {
    margin-top: -2px;
  }

  &__logo {
    height: 50px;
    width: 50px;
    margin-right: 10px;
  }

  &__image {
    height: 100%;
    width: 100%;
    object-fit: cover;
  }

  &__wrap {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 50%;
    flex: 1 1 auto;
  }

  &__buttons {
    display: flex;
    align-items: center;
    column-gap: 8px;
  }
}
</style>
