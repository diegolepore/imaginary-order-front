<template>
  <div class="container mx-auto px-8">
    <div class="md:w-9/12 mx-auto">
      <Nuxt />
    </div>
  </div>
</template>

<style>
html {
  font-family: 'Open Sans', sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

body {
  color: #2c3e50;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: 'Merriweather', serif;
  font-weight: bold;
} 

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

p {
  margin-bottom: 24px;
}

blockquote {
  margin-top: 41px;
  margin-bottom: 34px;
  font-size: 16px;
  font-weight: 400;
  border-left: 5px solid rgb(238, 238, 238);
  font-style: italic;
  padding: 10px 20px;
}

.article-body a {
  text-decoration: underline;
  color: #16a085;
}
</style>
