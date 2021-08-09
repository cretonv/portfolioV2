<template>
  <div class="container">
    <div class="content">
      <IconLogo class="logo" />
      <div class="left-part">
        <div class="text-content">
          <h1>Vincent Creton.</h1>
          <div class="sub-title">
            {{ subtitle }}
          </div>
          <div class="chapo">
            {{ chapo }}
          </div>
        </div>
      </div>
      <div class="right-part">
        <HomeIllustration />
      </div>
    </div>
  </div>
</template>

<script>
import IconLogo from '@/components/IconLogo'
import HomeIllustration from '@/components/HomeIllustration'
export default {
  head: {
    bodyAttrs: {
      class: 'no-margin'
    }
  },
  components: { IconLogo, HomeIllustration },
  data () {
    return {
      subtitle: 'Creative developer.',
      chapo: 'Jeune étudiant de 21 ans, je suis passionné par le développement web, nottament le développement front-end et le design web,'
    }
  }
}
</script>

<style scoped lang="scss">
.container {
  position: relative;
  display: flex;
  align-items: center;
  height: 100vh;
  background-color: #303030;

  .content {
    display: flex;
    flex-flow: row nowrap;
    color: #D9D9D9;
    margin: 0 auto;
    justify-content: space-around;
    width: 100%;

    .logo {
      position: absolute;
      left: calc(50% - 28px);
      top: 25px;
    }
    .right-part {
      width: 100%;
      padding-right: 50px;
    }
    .left-part {
      width: 100%;
      padding-left: 50px;

      .text-content {
        padding-left: 5vw;
      }
      h1 {
        font-family: 'Playfair';
        font-weight: 500;
        font-size: 85px;
        margin-top: 0;
        margin-bottom: 10px;
        max-width: 405px;
      }
      .sub-title {
        font-family: 'Lato';
        font-weight: 600;
        font-size: 39px;
        margin-bottom: 25px;
        max-width: 405px;
      }
      .chapo {
        font-family: 'Lato';
        font-size: 21px;
        font-weight: 300;
        max-width: 405px;
      }
    }
  }
}
</style>
