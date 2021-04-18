<template>
  <div class="Menu">
    <div>
      <nuxt-link class="Brand" to="/">
        <Logo></Logo>
        <span class="BrandTitle">DESING</span>
      </nuxt-link>
    </div>
    <div class="MenuOptions">
      <ul class="MenuOptionsUl">
        <li class="MenuOptionsLi">
          <NuxtLink to="/sobre-nosotros">Sobre nosotros</NuxtLink>
        </li>
        <li class="MenuOptionsLi">
          <nuxt-link to="/portafolio">Portafolio</nuxt-link>
        </li>
        <li class="MenuOptionsLi">
          <nuxt-link to="/planes">Planes</nuxt-link>
        </li>
        <li class="MenuOptionsLi">Contactanos</li>
      </ul>
    </div>
    <div class="ContainerMenu">
      <button class="bg-black hover:bg-gray-900 text-white font-100 py-2 px-4 rounded">Soy diseñador</button>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.Menu {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-height: 65px;
  padding: 10px 20px;
}


.Brand {
  display: flex;
  align-items: center;
}

.BrandTitle {
  margin-left: 5px;
  font-weight: bold;
  font-size: 1.1em;
  color: white;
}


.MenuOptionsUl {
  height: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-right: -1em;
}

.ContainerMenu {
  height: 100%;
}


.MenuOptionsLi {
  padding: 5px 10px;
  color: white;
}


</style>
