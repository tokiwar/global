<template>
  <nav class="navbar-main">
    <img class="navbar-main-img" src="~/assets/images/menu-line.png" alt=""/>
    <ul>
      <li @click="selectMenu" class="navbar-main-li-item real-item" data-number="01" data-label="Home">
        <span>01</span>
        <span class="navbar-main-li-item-dot is-active"></span>
        <span>Home</span>
      </li>
      <li v-for="n in 3" class="navbar-main-li-item"><span>&nbsp;</span><span
        class="navbar-main-li-item-dot is-transparent"></span><span>&nbsp;</span></li>
      <li @click="selectMenu" class="navbar-main-li-item not-active real-item" data-number="02" data-label="Works">
        <span></span>
        <span class="navbar-main-li-item-dot not-active"></span>
        <span>02</span>
      </li>
      <li v-for="n in 3" class="navbar-main-li-item"><span>&nbsp;</span><span
        class="navbar-main-li-item-dot is-transparent"></span><span>&nbsp;</span></li>
      <li @click="selectMenu" class="navbar-main-li-item not-active real-item" data-number="03" data-label="About">
        <span></span>
        <span class="navbar-main-li-item-dot not-active"></span>
        <span>03</span>
      </li>
      <li v-for="n in 3" class="navbar-main-li-item"><span>&nbsp;</span><span
        class="navbar-main-li-item-dot is-transparent"></span><span>&nbsp;</span></li>
      <li @click="selectMenu" class="navbar-main-li-item not-active real-item" data-number="04" data-label="Contact">
        <span></span>
        <span class="navbar-main-li-item-dot not-active"></span>
        <span>04</span>
      </li>
      <li v-for="n in 3" class="navbar-main-li-item"><span>&nbsp;</span><span
        class="navbar-main-li-item-dot is-transparent"></span><span>&nbsp;</span></li>
      <li @click="selectMenu" class="navbar-main-li-item not-active real-item" data-number="05" data-label="Hire us">
        <span></span>
        <span class="navbar-main-li-item-dot not-active"></span>
        <span>05</span>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "MainMenu",
  methods: {
    selectMenu(e) {
      let menuClickItems = document.querySelectorAll('li.real-item');
      if (menuClickItems) {
        let selectedItem = e.target;
        menuClickItems.forEach(item => {
          item.classList.remove('is-active');
          item.classList.add('not-active');
          item.childNodes[0].textContent = "";
          item.childNodes[item.childNodes.length - 1].textContent = item.dataset.number;
          item.querySelector('.navbar-main-li-item-dot').classList.remove('is-active');
          item.querySelector('.navbar-main-li-item-dot').classList.add('not-active');
        });
        if (!e.target.classList.contains('real-item')) {
          selectedItem = selectedItem.closest('.real-item');
        }
        if(selectedItem) {
          selectedItem.childNodes[0].textContent = selectedItem.dataset.number;
          selectedItem.childNodes[selectedItem.childNodes.length - 1].textContent = selectedItem.dataset.label;
          selectedItem.classList.remove('not-active');
          selectedItem.classList.add('is-active');
          selectedItem.querySelector('.navbar-main-li-item-dot').classList.add('is-active')
          selectedItem.querySelector('.navbar-main-li-item-dot').classList.remove('not-active')
        }
      }
    }
  }
}
</script>

<style scoped>
.navbar-main {
  color: white;
  user-select: none;
  position: relative;
}

.navbar-main-img {
  position: absolute;
  left: 76px;
}

.navbar-main li {
  list-style-type: none;
  font-family: ProximaLight, monospace;
  margin-top: 13px;
}

.navbar-main-li-item {
  width: 100px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}

.navbar-main-li-item.real-item {
  cursor: pointer;
}

.navbar-main-li-item-dot {
  height: 4px;
  width: 3px;
  background: white;
}

.navbar-main-li-item-dot.not-active {
  margin-right: 42.5px;
}

.navbar-main-li-item.not-active {
  justify-content: flex-start;
}

.navbar-main-li-item-dot.is-transparent {
  opacity: 0.4;
  margin-right: 26.1px;
}

.navbar-main-li-item-dot.is-active {
  background: #0f33ff;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}
</style>
