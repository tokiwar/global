<template>
  <div class="container">
    <div class="navbar">
      <MainMenu/>
    </div>
    <div class="content">
      <img src="~/assets/images/cosmo.png" alt=""/>
    </div>
  </div>
</template>

<script>
export default {
  name: "Container"
}
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 85%;
  margin-top:25px;
}
</style>
