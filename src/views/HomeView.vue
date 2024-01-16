<template>
  <v-app id="home">
    <NavBar />
    <v-container fluid class="pa-0">
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div class="container-text mt-16">
              <h2 class="text-white">Hello,</h2>
              <h2 class="text-white">I'M Christian Esposito</h2>
              <span class="text-white">Web Developer</span><br />
              <v-btn tile dark class="text-blue mt-8" variant="outlined">Contact Me</v-btn>
            </div>
          </v-col>
          <v-col cols="2">
            <!-- <div
              style="position:absolute; z-index:9999; bottom:0; margin-left:auto; margin-right:auto; left:0; right:0; text-align:center">
              <v-icon>fas fa-angle-double-down</v-icon>
            </div> -->
          </v-col>
          <v-col cols="5">
            <div style="position:relative; z-index: 9999;" class="mt-16">
              <v-img src="https://kgrassociates.com/wp-content/uploads/sites/36/2016/06/Happy-Business-Guy.jpg" contain
                max-height="300"></v-img>
            </div>
          </v-col>
        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="6">
              <div class="egg">
                <v-img src="https://kgrassociates.com/wp-content/uploads/sites/36/2016/06/Happy-Business-Guy.jpg"
                  max-height="200"></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h2 class="mb-2">About Me</h2>
              <h4 class="mb-4">I Am a Web Developer</h4>
              <div style="width:40em">
              <p class="text-grey" >
                Sono Christian Esposito, uno sviluppatore web appassionato con un occhio attento
                per la creatività. La mia competenza principale risiede nello sviluppo web,
                dove ho accumulato esperienza in progetti significativi,
                dimostrando una solida padronanza delle tecnologie Front-End
              </p>
                <br/>
              <p class="text-grey" >
                Oltre al mondo del codice, coltivo la passione per la fotografia, trovando ispirazione nell'arte di
                catturare momenti unici,
                In aggiunta l'amore per le moto non è solo un hobby,
                ma un modo di abbracciare l'innovazione e l'avventura.
                La capacità di affrontare sfide, la precisione e l'attenzione ai dettagli acquisite sui percorsi
                in moto si riflettono nel mio approccio al lavoro.
              </p>
              <v-btn tile dark color="blue" class="mt-4"> Download CV</v-btn>
            </div>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <div class="text-center mt-4">
        <h2>Cosa Faccio</h2>
      </div>
      <v-col cols="12" class="padd" id="portfolio">
        <div class="first" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child">
                 <v-btn icon="fas fa-laptop" color="blue" class="text-white"></v-btn>
                 <h3 class="ml-3 mt-4">Web Developer</h3>
                 <p class="text-grey ml-3 mt-4 text-caption">
                  Progetti creati come Web Developer
                 </p>
              </div>
              <!-- <div class="child">
                <v-btn icon="fas fa-camera" color="blue" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">Fotografia</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                 Di seguito alcuni miei Scatti come Fotografo
                </p>
             </div> -->
            </v-col>
          </v-row>
          <v-divider></v-divider>
        </div>
      </v-col>
    </v-container>
  </v-app>
</template>

<script>
import { defineComponent } from 'vue'

// Components
import NavBar from '@/components/NavBar.vue'

export default defineComponent({
  name: 'HomeView',

  components: {
    NavBar
  }
})
</script>

<style scoped>
.v-container {
  padding: 0 !important;
}

.head {
  position: relative;
  text-align: center;
  padding: 12px;
  margin-bottom: 6px;
  height: 400px;
  width: 100%;
  color: white;
}

.head:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background-color: black;
  transform: skew(0deg, 3deg);
}

.head:after {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 50%;
  background-color: black;
  transform: skew(0deg, 6deg);
}

.container-text {
  position: relative;
}

.egg {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-left: 100px;
  margin-top: 50px;
  width: 356px;
  height: 300px;
  background-color: #FBDF7F;
  border-radius: 50%;
  text-align: center;
}

.first{
  whidt:100%;
  height: 280px;
  text-align: center;
  padding: 2rem 2rem;
}

.child{
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: center;
  margin-right: 8px;
}

.imgHover{
  padding: 0 200px;
}
.pre{
  width: 100%;
  height: 380px;
  text-align: center;
  padding: 0 200px;
  background-color: #f5f5f5;
}
.hire{
width: 100%;
height: 200px;
padding: 0 200px;
background-color: #e9e9e9;
margin-top: -24px;
}
</style>
