<template>
  <div class="container">
    <div class="photo-part">
      <img :src="require(`~/assets/img/me.jpeg`)">
    </div>
    <div class="text-part">
      Jeune étudiant de 21 ans, je suis passionné par le développement web, nottament le développement front-end et le design web, depuis ma découverte de cet univers durant mon DUT MMI. Mon DUT en poche, j’ai poursuivi mon cursus en Bachelor développeur interactif aux Gobelins, formation suivi en alternance dans l’entreprise Herewecom.
      Je compte désormais continuer de me spécialiser dans ce domaine en suivant le Master Design et Management de l'innovation interactive dans la même école.
    </div>
  </div>
</template>

<script>
export default {
  name: 'Presentation'
}
</script>

<style lang="scss" scoped>
.container {
  display: flex;
  flex-flow: row nowrap;
  max-width: 815px;
  margin: 0 auto;
  .photo-part {
    width: 200px;
    height: 200px;
    border-radius: 200px;
    img {
      object-fit: cover;
      object-position: center;
      width: 200px;
      height: 200px;
      border-radius: 200px;
    }
  }
  .text-part {
    font-family: Lato;
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
    color: #303030;
    padding: 16px;
    background-color: #D9D9D9;
    box-shadow: 0 46px 49px -2px rgba(0,0,0,0.15), 0 6px 6px -2px rgba(0,0,0,0.14), 0 2px 2px -2px rgba(0,0,0,0.13), 0 0 5px 0 rgba(171,171,171,0.50), inset 0 2px 1px 0 rgba(255,255,255,0.75);
    border-radius: 8px;
    margin-left: 16px;
  }
}
</style>
