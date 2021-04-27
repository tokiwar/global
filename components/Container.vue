<template>
  <div class="container">
    <div class="navbar">
      <MainMenu/>
    </div>
    <div class="content">
      <div class="content-top">
        <div class="content-top-left">
          <span class="content-top-left-text">Your next interactive experience</span>
          <button class="content-top-left-button">
            <img src="~/assets/images/button-arrow.png" alt=""/>
          </button>
        </div>
        <div class="content-top-right">
          <img src="~/assets/images/cosmo.png" alt=""/>
        </div>
      </div>
      <div class="content-bottom">
        <img src="~/assets/images/content-divider.png" alt=""/>
        <div class="content-bottom-tabs">
          <div class="content-bottom-tabs-item is-active" @click="selectTab">
            <div class="content-bottom-tabs-item-selector"></div>
            <div class="content-bottom-tabs-item-title">METTIEW & SMITH</div>
            <div class="content-bottom-tabs-item-text">Lorem ipsum dolor sit amet, consectetur <br> adipisicing elit,
              sed do eiusmod tempor
            </div>
          </div>
          <div class="content-bottom-tabs-item" @click="selectTab">
            <div class="content-bottom-tabs-item-selector"></div>
            <div class="content-bottom-tabs-item-title">FANTASY INTERACTIVE</div>
            <div class="content-bottom-tabs-item-text">Lorem ipsum dolor sit amet, consectetur <br> adipisicing elit,
              sed do eiusmod tempor
            </div>
          </div>
          <div class="content-bottom-tabs-item" @click="selectTab">
            <div class="content-bottom-tabs-item-selector"></div>
            <div class="content-bottom-tabs-item-title">PAUL & SHARK</div>
            <div class="content-bottom-tabs-item-text">Lorem ipsum dolor sit amet, consectetur <br> adipisicing elit,
              sed do eiusmod tempor
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Container",
  methods: {
    selectTab(e) {
      let tabsItems = document.querySelectorAll('.content-bottom-tabs-item');
      if (tabsItems) {
        tabsItems.forEach(item => {
          item.classList.remove('is-active');
        })
        let selectedItem = e.target;
        if (!e.target.classList.contains('content-bottom-tabs-item')) {
          selectedItem = selectedItem.closest('.content-bottom-tabs-item');
        }
        if (selectedItem) {
          selectedItem.classList.add('is-active');
        }
      }
    },
  }
}
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 95%;
  margin-top: 25px;
  align-self: center;
}

.navbar {
  width: 100%;
  display: flex;
  align-items: center;
}

.content {
  display: flex;
  flex-direction: column;
  width: fit-content;
}

.content-top {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  width: fit-content;
}

.content-top-left {
  display: flex;
  flex-direction: column;
}

.content-top-right{
  display: flex;
  position: relative;
  right: 55px;
}

.content-top-left-text {
  color: white;
  font-size: 82px;
  font-family: ProximaBlack, monospace;
  margin-top: 25px;
  line-height: 75px;
}

.content-top-left-button::before {
  display: inline-block;
  right: 31%;
  width: 100%;
  position: absolute;
  content: "HIRE US";
}

.content-top-left-button {
  cursor: pointer;
  position: relative;
  display: flex;
  width: 100px;
  height: 36px;
  margin-top: 60px;
  background: #0f33ff;
  border: none;
  color: white;
  font-family: ProximaBold, monospace;
  font-size: 16px;
  padding-left: 18%;
  place-items: center;
  margin-left: 12px;
}

.content-bottom-tabs {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  color: white;
  margin-top: -6px;
}

.content-bottom {
  margin-top: -15px;
}

.content-bottom-tabs{
  margin-right: 30px;
}

.content-bottom-tabs-item {
  cursor: pointer;
  opacity: 0.1;
}

.content-bottom-tabs-item.is-active {
  opacity: 1;
}

.content-bottom-tabs-item-selector {
  width: 35px;
  height: 6px;
  background: #0f33ff;
  visibility: hidden;
}

.content-bottom-tabs-item.is-active .content-bottom-tabs-item-selector {
  visibility: unset;
}

.content-bottom-tabs-item-title {
  font-family: ProximaBold monospace;
  margin-top: 25px;
  font-size: 20px;
}

.content-bottom-tabs-item-text {
  margin-top: 25px;
  font-family: ProximaRegular monospace;
  line-height: 25px;
}

</style>
