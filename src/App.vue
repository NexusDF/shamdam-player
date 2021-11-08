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
          <img class="artist__image" src="./assets/anime.jpg" />
        </div>
        <div class="artist__header">
          <div class="top">
            <span class="top__who">ИСПОЛНИТЕЛЬ</span>
            <h1 class="top__name">MC СНЮС</h1>
            <span class="top__like">Нравится всем</span>
          </div>
          <div class="bottom">
            <div class="bottom__listen-like">
              <button class="bottom__listen">
                <span class="listen">
                  <VIcon name="play_arrow" size="24" />
                  <span>Слушать</span>
                </span>
              </button>
              <button class="bottom__like">
                <span class="like">
                  <VIcon name="favorite_border" size="24" />
                  <span class="count-like">1488</span>
                </span>
              </button>
              <button class="bottom__share">
                <VIcon name="share" size="24" />
              </button>
            </div>
            <div class="bottom__radio-not">
              <button class="bottom__radio">
                <span class="radio">
                  <VIcon name="podcasts" size="24" />
                  Радио
                </span>
              </button>
              <button class="bottom__not-recom">
                <VIcon name="block" size="24" />
              </button>
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
                  <div class="song-buttons">
                    <button class="song-buttons__download">
                      <VIcon name="download" size="28" />
                    </button>
                    <button class="song-buttons__like">
                      <VIcon name="favorite_border" size="28" />
                    </button>
                    <div class="song-button__time">
                      <span>4:20</span>
                    </div>
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
    margin-left: 10px;
  }

  button {
    height: 40px;
  }
}

.top {
  width: 100%;

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
}

.bottom {
  width: 100%;
  display: flex;
  justify-content: space-between;

  &__listen-like {
  }

  &__listen {
    background-color: $second;
    border-radius: 20px;
    border: none;
    width: 100px;
    font-size: 13px;
    margin-right: 10px;

    .listen {
      display: flex;
      justify-content: center;
      align-items: center;
    }

    &:hover {
      background-color: $hoverYellow;
    }
  }

  &__like {
    border-radius: 20px;
    border: solid 1px $greyHover;
    max-width: 200px;
    min-width: 100px;
    margin-right: 10px;
    background-color: white;

    &:hover {
      border-color: $grey;
    }

    .like {
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .count-like {
      margin-left: 5px;
      font-size: 15px;
    }
  }

  &__share {
    width: 40px;
    border-radius: 50%;
    border: solid 1px $greyHover;
    background-color: white;

    &:hover {
      border-color: $grey;
    }
  }

  &__radio-not {
    button {
      background-color: white;
      border: solid 1px $greyHover;
      border-radius: 20px;
      margin-left: 10px;
    }
    button:hover {
      border-color: $grey;
    }
  }

  &__radio {
    width: 90px;

    .radio {
      display: flex;
      justify-content: center;
      align-items: center;
    }
  }

  &__not-recom {
    width: 40px;

    span {
      display: flex;
      justify-content: center;
    }
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
    align-items: center;
    width: 50%;
    flex: 1 1 auto;
  }

  &__name {
  }

  &__buttons {
    display: flex;
    align-items: center;

    button {
      border: none;
      background: none;
      color: $spanGrey;
      margin-right: 15px;
    }

    button:hover {
      color: black;
    }
  }
}

.song-buttons {
  min-width: 100px;
  display: flex;
  align-items: center;
}

.list-song:hover {
  border: solid 2px $second;
  padding: 5px;
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
