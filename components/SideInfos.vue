<template>
  <div class="infos-container">
    <div class="infos-item">
      étudiant aux gobelins
    </div>
    <div class="infos-item">
      grenoble / annecy
    </div>
    <div class="infos-item">
      dévelopeur à herewecom
    </div>
  </div>
</template>

<script>
export default {
  name: 'SideInfos'
}
</script>

<style scoped>
.infos-item {
  font-size: 14px;
  font-weight: 200;
  color: #ffffff;
  font-family: 'Lato';
}
.infos-container {
  width: 100vh;
  position: absolute;
  display: flex;
  flex-flow: row nowrap;
  justify-content: space-around;
  text-transform: uppercase;
  top: 0;
  left: 26px;
  transform-origin: top left;
  transform: rotate(-90deg) translateX(-100vh);
}
</style>
