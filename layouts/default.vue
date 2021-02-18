<template>
  <div>
    <Nuxt />
  </div>
</template>

<script>
export default {
  head() {
    return {
      link: [
        {
          rel: 'stylesheet',
          href: 'https://fonts.googleapis.com/css2?family=Roboto+Mono:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;1,100;1,200;1,300;1,400;1,500;1,600;1,700&display=swap'
        }
      ]
    }
  }
}
</script>
<style>
html {
  font-family: 'Roboto Mono', monospace;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  overflow: hidden;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
h1, h2, h3, h4, p, span, label, a {
    background: linear-gradient(180deg, white 10%, #7ac2d4 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}
</style>
