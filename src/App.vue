<template>
  <div class="container">
    <div class="header">
      <div class="header__logo">
        <VIcon name="music_note" size="32" />
        <span class="header__title">ShamDam Player</span>
      </div>
    </div>
    <div class="wrapper">
      <div class="artist">
        <div class="artist__logo">
          <img
            class="artist__image"
            src="https://avatars.mds.yandex.net/i?id=d80edbf6070eb7e56c69595ed59b849b-5354907-images-thumbs&n=13&exp=1"
          />
        </div>
        <div class="artist__header">
          <div class="top">
            <span class="top__who">ИСПОЛНИТЕЛЬ</span>
            <h1>MC СНЮС</h1>
            <span class="top__like">Нравится всем</span>
          </div>
          <div class="bottom">
            <div class="bottom__listen-like">
              <button class="bottom__listen">Слушать</button>
              <button class="bottom__like"></button>
              <button class="bottom__share"></button>
            </div>
            <div class="bottom__radio-not">
              <button class="bottom__radio">Радио</button>
              <button class="button__not-recom"></button>
            </div>
          </div>
        </div>
      </div>
      <div class="menu"></div>
      <div class="list-of-songs">
        <div class="list-top">
          <h2 class="list-top__header">Популярные треки</h2>
          <span class="list-top__see-all">Смотреть все</span>
        </div>
        <div class="list-of-songs__list">
          <ul class="list-of-songs__list-song">
            <li class="list-song">
              <div class="list-song__logo">
                <img
                  src="https://al-school.ru/wp-content/uploads/2019/12/Granit-Vit-Portion-Snus-Open.jpg"
                  alt=""
                />
              </div>
              <div class="list-song__wrap">
                <div class="list-song__name">
                  <span class="list-song__title">
                    MC Снюс - Снюс is my life
                  </span>
                </div>
                <div class="list-song__buttons">
                  <div>
                    <button>Like</button>
                    <button>Скачать</button>
                  </div>
                  <div>
                    <span>Time</span>
                  </div>
                </div>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="player-controller">
      <button class="player-controller__prev">
        <VIcon name="fast_rewind" size="28" />
      </button>
      <button class="player-controller__play">
        <VIcon name="play_arrow" size="28" />
      </button>
      <button class="player-controller__next">
        <VIcon name="fast_forward" size="28" />
      </button>
      <button class="player-controller__queue">
        <VIcon name="queue_music" size="28" />
      </button>
      <button class="player-controller__mute">
        <VIcon name="volume_up" size="28" />
      </button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projectTitle: "ShamDam Player",
    };
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

.header {
  width: 100%;
  height: 70px;
  color: $fontColor;
  border-bottom: solid 1px $borderColor;
  padding: 12px;

  &__logo {
    display: flex;
    align-items: center;
    height: 100%;
    gap: 6px;
  }

  &__title {
    font-size: 1.2rem;
  }
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

    img {
      width: 200px;
      height: 200px;
      border-radius: 50%;
      object-fit: cover;
    }
  }

  &__header {
    display: flex;
    flex-direction: column;
    width: 100%;
    justify-content: space-between;
  }
}

.top {
  width: 100%;
}

.bottom {
  width: 100%;
  display: flex;
  justify-content: space-between;
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
}

.list-song {
  display: flex;
  align-items: center;
  padding: 7px;
  height: 50px;
  width: auto;
  justify-content: space-between;

  &__logo {
    height: 50px;
    width: 50px;
    margin-right: 10px;

    img {
      height: 100%;
      width: 100%;
      object-fit: cover;
    }
  }

  &__wrap {
    display: flex;
    justify-content: space-between;
    width: 50%;
    flex: 1 1 auto;
  }

  &__name {
  }

  &__buttons {
    display: flex;
  }
}

.list-song:hover {
  border: solid 2px $second;
}

.player-controller {
  position: fixed;
  height: 70px;
  bottom: 0;
  max-width: 1140px;
  width: 100%;
  margin: 0 auto;
  border-top: solid 10px $borderColor;
  display: flex;
  align-items: center;

  &__mute {
    margin-left: auto;
  }

  button {
    border: none;
    background-color: transparent;
    padding: 12px;
    color: $grey;
  }

  button:hover {
    color: #123;
  }
}
</style>
