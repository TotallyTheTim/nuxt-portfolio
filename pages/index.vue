<template>
  <div id="main">
    <intro />
    <about />
    <skills />
  </div>
</template>

<script>
import intro from '~/components/intro.vue'
import about from '~/components/projects.vue'
import skills from '~/components/skills.vue'

export default {
  components: {
    intro,
    about,
    skills
  }
}
</script>

<style lang="scss">
$dark: #313131;
$darker: #2c2c2c;
$theme: #ff9900;
$light: #e1e1e1;

body {
  background-color: $darker;
  overflow-x: hidden;

  #__nuxt:after {
    content: '';
    display: block;
    height: calc(100vh + 100vw);
    width: calc(100vh + 100vw);
    border-radius: 100%;
    background: $theme;
    position: absolute;
    top: calc(calc(100vh + 100vw) / -4);
    right: calc(calc(60vh + 60vw) / -1);
  }
}

.btn {
  padding: 24px 48px;
  min-width: 300px;
  font-weight: lighter;
  font-size: 32px;
  border-radius: 32px;
  background: none;
  border: solid 2px $theme;
  color: $theme;
}

#main {
  position: relative;
  z-index: 1;

  > div {
    overflow: hidden;
    min-height: 100vh;
    padding: 48px;

    .intro {
      min-height: calc(100vh - 48px - 48px);
      display: flex;
      flex-direction: row;

      .intro-text {
        flex: 1 0 50%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: flex-start;
        * {
          color: $light;
          margin: 8px 0;
        }
        span {
          font-weight: normal;
          font-size: 42px;
        }
        h1,
        h2 {
          font-weight: bold;
          color: $theme;
          font-size: 72px;
        }
        h3,
        h4 {
          font-weight: normal;
          font-size: 42px;
        }
      }

      .intro-image {
        flex: 1 0 50%;
        position: relative;
      }

      .handsome-guy {
        width: calc(35vh + 35vw);
        position: absolute;
        bottom: -48px;
        right: -48px;
        transform: scale(-1, 1) translate(0, 10%);
      }
    }

    &:nth-child(even) {
      background-color: $dark;
    }
  }
}
</style>
