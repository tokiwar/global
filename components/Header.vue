<template>
  <div class="header">
    <div class="header-top">
      <div class="logo">
        <img src="~/assets/images/logo.png" alt=""/>
        <span class="logo-text">GLOBAL</span>
      </div>
      <div class="burger">
        <img src="~/assets/images/burger.png" alt=""/>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header"
}
</script>

<style scoped>

.header {
  display: flex;
  justify-content: center;
}

.header-top {
  width: 85%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin-top: 25px;
  margin-bottom: 25px;
}

.logo {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content:space-between;
}

.logo-text {
  color: white;
  margin-left: 10px;
  font-size: 17px;
}
</style>
