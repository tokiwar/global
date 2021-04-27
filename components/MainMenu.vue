<template>
  <nav>
    <img class="nav-line-img" src="~/assets/images/menu-line.png" alt=""/>
    <ul>
      <li>
        <a href="#home" class="nav-line-item-real">
          <div class="nav-line-item"><span>01</span><span>Home</span></div>
        </a>
      </li>
      <li>
        <div class="nav-line-item-none"></div>
      </li>
      <li>
        <div class="nav-line-item-none"></div>
      </li>
      <li>
        <div class="nav-line-item-none"></div>
      </li>
      <li>
        <a href="#works" class="nav-line-item-real">
          <div class="nav-line-item"><span>02</span><span>Works</span></div>
        </a>
      </li>
      <li>
        <div class="nav-line-item-none"></div>
      </li>
      <li>
        <div class="nav-line-item-none"></div>
      </li>
      <li>
        <div class="nav-line-item-none"></div>
      </li>
      <li>
        <a href="#about" class="nav-line-item-real">
          <div class="nav-line-item"><span>03</span><span>About</span></div>
        </a>
      </li>
      <li>
        <div class="nav-line-item-none"></div>
      </li>
      <li>
        <div class="nav-line-item-none"></div>
      </li>
      <li>
        <div class="nav-line-item-none"></div>
      </li>
      <li>
        <a href="#contact" class="nav-line-item-real">
          <div class="nav-line-item"><span>04</span><span>Contact</span></div>
        </a>
      </li>
      <li>
        <div class="nav-line-item-none"></div>
      </li>
      <li>
        <div class="nav-line-item-none"></div>
      </li>
      <li>
        <div class="nav-line-item-none"></div>
      </li>
      <li>
        <a href="#hire" class="nav-line-item-real">
          <div class="nav-line-item"><span>05</span><span>Hire us</span></div>
        </a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "MainMenu"
}
</script>

<style scoped>
nav {
  height: 100%;
  margin-top: 40px;
  position: relative;
}

.nav-line-img {
  position: absolute;
  left: 55%;
  top: -10%;
}

.nav-line-item {
  display: flex;
  flex-direction: row;
  width: 100px;
  justify-content: space-between;
}

ul {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100%;
}

li {
  font-family: ProximaLight, monospace;
  font-size: 16px;
  list-style-type: none;
}

li a {
  text-decoration: none;
  color: white;
}
</style>
