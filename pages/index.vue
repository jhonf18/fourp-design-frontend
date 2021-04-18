<template>
  <div>
    <div class="Top">
      <div class="TopBackground">
        <div class="container">
          <Menu></Menu>
        </div>
      <div class="TopBackgroundBlack">
        <div class="ContentTop">
          <h2 class="TopTitle">
            ¡UNA MIRADA HACIA LO DIFERENTE!
          </h2>
          <div class="TopBody">
            <p>Un buen diseñador ayuda a vender más, y nosotros somos expertos en diseñar.</p>
            <p class="mt-3">¡NO ESPERES MÁS Y TRABAJEMOS JUNTOS!</p>
          </div>
          <div class="TopBotton">
            <button class="BottonColor text-white font-bold py-2 px-4 rounded">
              CONTACTANOS
            </button>
          </div>
        </div>
      </div>
      </div>
    </div>
    <Footer></Footer>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>

.container {
  margin: auto;
}

.TopBackground {
  background-image: linear-gradient(#BB49FF, #230137);
  padding-bottom: 5px;
}

.TopBackgroundBlack {
  background-color: black;
  padding: 20px;
  margin-top: -65px;
  width: 60%;
  margin-bottom: 20px;
}

.ContentTop {
  margin-top: 65px;
  padding: 2em 1.4em 5.5em  1.4em;
}

.TopTitle {
  margin-top: 20px;
  color: white;
  font-weight: bold;
  font-size: 2.85em;
  line-height: 1.2em;
}

.TopBody {
  margin-top: 2em;
  color: white;
  font-size: 1.2em;
}

.TopBotton {
  margin-top: 2.5em;
}

.BottonColor {
  background-image: linear-gradient(to right,#BB49FF, #230137);
}

</style>
