<template>
  <div>
    <div class="TopBackground content-top">
      <div class="container">
        <Menu></Menu>
      </div>
      <div class="TopContent">
        <h2 class="TopTitle font-bold">¡Nunca pares de crecer!</h2>
        <p class="TopBody">
          Nuestros trabajos son realizados con calidad y pasión, con el objetivo de ofrecerte el mejor servicio.
        </p>
      </div>
    </div>
    <Tabs>
      <Tab :name="category.name" v-for="category in  categories" :key="category.code">
        <div style="background-color: #000" class="pt-5">
          <div class="container m-auto m-auto grid grid-cols-2 md:grid-cols-2 sm:grid-cols-2 xl:grid-cols-4 gap-2 lg:gird-cols-4">
            <div v-for="project in category.projects" :key="project.id" class="ProjectContainer" >
              <div class="text-white">
                <div class="ProjectHeader">
                  <img :src="project.image" :alt="'Projecto sobre ' + project.name " class="ProjectImg">
                </div>
                <div>
                  <span class="font-bold">{{ project.name }}</span>
                  <br style="height: 10px">
                  <span class="font-extralight block" style="margin-top: -5px; margin-left: 3px">{{ project.name_designer }}</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </Tab>
    </Tabs>
    <Footer></Footer>
  </div>
</template>


<script>
export default {
  data(){
    return {
      categories: [
        {
          name: 'Arquitectónico',
          code: 1,
          projects: [
            {
              id: 'sd',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas 1',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            },
            {
              id: '1',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas 2',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            },
            {
              id: '132',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas 1',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            },
            {
              id: '1232',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas 2',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            },
            {
              id: '3213',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas 1',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            },
            {
              id: '13232',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas 2',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            }
          ]
        },
        {
          name: 'Interiores',
          code: 2,
          projects: [
            {
              id: '2',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            },
            {
              id: '3',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            }
          ]
        },
        {
          name: 'Industrial',
          code: 3,
          projects: [
            {
              id: '4',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            },
            {
              id: '5',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            }
          ]
        },
        {
          name: 'Modas',
          code: 4,
          projects: [
            {
              id: '6',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            },
            {
              id: '7',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            }
          ]
        },
        {
          name: 'Editorial',
          code: 5,
          projects: [
            {
              id: '8',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            },
            {
              id: '9',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            }
          ]
        },
        {
          name: 'Web',
          code: 6,
          projects: [
            {
              id: '10',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            },
            {
              id: '11',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            }
          ]
        },
        {
          name: 'Ilustración',
          code: 7,
          projects: [
            {
              id: '12',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            },
            {
              id: '13',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            }
          ]
        },
        {
          name: 'Marcas',
          code: 8,
          projects: [
            {
              id: '14',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            },
            {
              id: '15',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            }
          ]
        },
        {
          name: 'Multimedia',
          code: 9,
          projects: [
            {
              id: '16',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            },
            {
              id: '17',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            }
          ]
        },
        {
          name: 'Animación',
          code: 10,
          projects: [
            {
              id: '18',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            },
            {
              id: '19',
              name_designer: 'Mario Ospina Rojas',
              name: 'Paredes guapas',
              image: 'https://definicion.xyz/wp-content/uploads/2020/11/diseno-arquitectonico-700x438.jpg'
            }
          ]
        }
      ]
    }
  }
}
</script>


<style scoped>
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

.ProjectContainer {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  border-radius: 3px;
  overflow: hidden;
  padding-bottom: 1em;
}
.ProjectHeader  {
  height: calc(100% - 50px);
}

.ProjectImg {
  width: 100%;
  height: 100%;
}

</style>
