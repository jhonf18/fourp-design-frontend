<template>
  <div class="Footer ">
    <div class="container FooterContainer">
      <div class="Brand flex">
      <Logo></Logo>
      <span class="BrandTitle">DESING</span>
    </div>
    <div class="Extensions">
      <h4>Extensiones</h4>
      <ul>
        <li>
          <a href="https://fourp.space" target="_blank">FourP</a>
        </li>
        <li>
          <nuxt-link to="/">Desing</nuxt-link>
        </li>
      </ul>
    </div>
    </div>

  </div>
</template>

<style scoped>

.Footer {
  background-image: linear-gradient(to top,#BB49FF, #230137);
}

.FooterContainer {
  display: flex;
  padding: 2.5em 20px;
  padding-bottom: 4em;
}

.Brand {
  align-items: center;
}

.BrandTitle {
  margin-left: 10px;
  font-weight: bold;
  font-size: 1.1em;
  color: white;
  font-size: 1.5em;
}

.Extensions {
  margin-left: 3em;
  color: #fff;
}

.Extensions h4 {
  font-weight: bold;
  margin-bottom: 1em;
}
</style>
