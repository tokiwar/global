<template>
  <div>
    <Nuxt/>
  </div>
</template>

<style>
@font-face {
  font-family: 'Avenir';
  src: url('~assets/fonts/Avenir-Black.woff') format('truetype');
}

@font-face {
  font-family: 'ProximaBlack';
  src: url('~assets/fonts/Proxima-Nova-Black.woff') format('truetype');
}

@font-face {
  font-family: 'ProximaLight';
  src: url('~assets/fonts/Proxima-Nova-Light.woff') format('truetype');
}

@font-face {
  font-family: 'ProximaBold';
  src: url('~assets/fonts/Proxima-Nova-Bold.woff') format('truetype');
}

@font-face {
  font-family: 'ProximaRegular';
  src: url('~assets/fonts/Proxima-Nova-Regular.woff') format('truetype');
}

html {
  background: black;
  font-family: Avenir, monospace;
}

button:focus,
button:active {
  outline: none;
}
</style>
