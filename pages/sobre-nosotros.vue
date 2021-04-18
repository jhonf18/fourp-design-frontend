<template>
  <div>
    <div class="TopBackground">
      <div class="container">
        <Menu></Menu>
      </div>
      <div class="TopContent">
        <h2 class="TopTitle font-bold">¡Nuestros Freelances!</h2>
        <p class="TopBody">
          Nuestros Freelances cuentan con una excelente preparación para ofrecer el mejor servicio a nuestros usuarios.
        </p>
      </div>
    </div>
    <div class="Team">
      <h2 class="text-white TeamTitle font-semibold text-center">Nuestro Equipo</h2>
      <div class="TeamContainer grid grid-cols-1 md:grid-cols-2 sm:grid-cols-1 xl:grid-cols-3 lg:gird-cols-3">
        <div v-for="person in team" :key="person.id"  class="mt-3">
          <div class="card-person  flex justify-center items-center">
            <div class="card-person-container">
              <div class="container-photo">
                <div class="container-photo-in">
                  <img :src="person.photo" :alt="'Foto de' + person.name" class="photo">
                </div>
              </div>
              <div>
                <p class="mt-2 text-center">
                  <span class="font-bold">{{ person.title }}</span>
                  <br>
                  <span>{{person.name}}</span>
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <Footer></Footer>
  </div>
</template>

<script>
export default {
  data(){
    return {
      team: [
        {
          name: 'Juan Lopez Mercedez',
          title: 'Diseñador web',
          photo: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRQRU2fqzA3oHfjjb8leH3AHDoJGUz5OCFAPg&usqp=CAU',
          id: '1'
        },
        {
          name: 'Mario Ospina Rojas',
          title: 'Ilustrador',
          photo: 'https://lamenteesmaravillosa.com/wp-content/uploads/2018/09/hombre-creido-pensando-que-sabe.jpg',
          id: '2'
        },
        {
          name: 'Carlos Ernesto Carvajal',
          title: 'Diseño 3D',
          photo: 'https://img.freepik.com/foto-gratis/retrato-joven-sonriente-gafas_171337-4842.jpg?size=626&ext=jpg',
          id: '3'
        },

        {
          name: 'Carlos Ernesto Carvajal',
          title: 'Diseño 3D',
          photo: 'https://img.freepik.com/foto-gratis/retrato-joven-sonriente-gafas_171337-4842.jpg?size=626&ext=jpg',
          id: '4'
        },
        {
          name: 'Mario Ospina Rojas',
          title: 'Ilustrador',
          photo: 'https://lamenteesmaravillosa.com/wp-content/uploads/2018/09/hombre-creido-pensando-que-sabe.jpg',
          id: '5'
        }
      ]
    }
  }
}
</script>


<style scoped lang="scss">

@mixin photos($size_box) {
  .card-person {
    &-container {
      width: 100%;
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      .container-photo {
        width: $size_box;
        height: $size_box;
        border-radius: 50%;
        background-image: linear-gradient(to bottom, #BB49FF, #230137);
        transition: all 3s;
        display: flex;
        justify-content: center;
        align-items: center;
        overflow: hidden;
        &:hover {
          background: linear-gradient(to bottom,#bc49ff83, #23013771);
        }
        &-in {
          cursor: pointer;
          width: $size_box - 15px;
          height: $size_box - 15px;
          border-radius: 50%;
          img {
            width: 100%;
            height: 100% !important;
            border-radius: 50%;
          }
        }
      }
    }
  }
}

.container {
  margin: auto;
}

.TopBackground {
  background-image: linear-gradient(#BB49FF, #230137);
  padding-bottom: 4em;
}

.TopContent {
  color: #fff;
  text-align: center;
  max-width: 500px;
  margin: auto;
  margin-top: 4em;
}

.TopBody {
  line-height: 1em;
}

.TopTitle {
  font-size: 2.2em;
  margin-bottom: 1em;
}

.Team {
  padding: 2em 0;
  background-color: #000;
}

.TeamTitle {
  font-size: 1.6em;
}

.TeamContainer {
  margin-top: 2.4em;
  color: #fff;
}

@media (max-width: 400px){
  @include photos($size_box: 150px);
}


@media (min-width: 401px) {
  @include photos($size_box: 180px)
}


</style>
