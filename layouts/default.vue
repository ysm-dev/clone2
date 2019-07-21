<template>
  <nuxt />
</template>

<style lang="scss">
@import '../node_modules/normalize.css/normalize.css';

html {
  box-sizing: border-box;
  font-weight: 500;
  font-size: 16px;
  font-family: Roboto, 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial,
    sans-serif;
  /* word-spacing: 1px; */

  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
}
*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;

  scrollbar-width: none;
}
body {
  background: #fafafa;
}
html,
body,
#__nuxt {
  overflow: hidden;
  height: 100%;
}
#__layout {
  overflow: hidden;
  height: 100%;
}

::-webkit-scrollbar {
  width: 0px;
  background: transparent;
}
</style>
