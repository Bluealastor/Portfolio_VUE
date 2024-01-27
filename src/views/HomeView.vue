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
              <v-img src="../assets/Photo.jpg" contain
                max-height="300"></v-img>
            </div>
          </v-col>
        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="about">
        <AboutComponentView/>
      </v-col>
      <div class="text-center mt-4">
        <h2>Cosa Faccio</h2>
      </div>
      <v-col cols="12" class="padd" id="portfolio">
        <div class="first" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child mx-auto my-auto text-center">
                <v-img src="../assets/icon/development.png"  height="3em" class="text-white"></v-img>
                <h3 >Web Developer</h3>
                <!-- <p class="text-grey ml-3 mt-4 text-caption">
                  Progetti creati come Web Developer
                </p> -->
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
      <v-col cols="12" sm="12" id="services">
        <div class="d-flex justify-center mb-6">
          <div color="blue" class="mr-2 d-flex flex-wrap justify-center " style="margin:20px; width:5em">Angular <v-img width="3em" src="../assets/icon/angular.svg"/></div>
          <div color="blue" class="mr-2 d-flex flex-wrap justify-center " style="margin:20px; width:5em">React <v-img width="3em" src="../assets/icon/react.png"/></div>
          <div color="blue" class="mr-2 d-flex flex-wrap justify-center " style="margin:20px; width:5em">JavaScript <v-img width="3em" src="../assets/icon/javascript.png"/></div>
          <div color="blue" class="mr-2 d-flex flex-wrap justify-center " style="margin:20px; width:5em">HTML5 <v-img width="3em" src="../assets/icon/html-5.png"/></div>
          <div color="blue" class="mr-2 d-flex flex-wrap justify-center " style="margin:20px; width:5em">Css3 <v-img width="3em" src="../assets/icon/css.png"/></div>
          <div color="blue" class="mr-2 d-flex flex-wrap justify-center " style="margin:20px; width:5em">Bootstrap <v-img width="3em" src="../assets/icon/bootstrap.png"/></div>
        </div>
      </v-col>
      <v-col cols="12" class="imgHover">
        <PortfolioView/>
      </v-col>
    </v-container>
  </v-app>
  <FooterView />
</template>

<script>
import { defineComponent } from 'vue'

// Components
import NavBar from '@/components/NavBar.vue'
import PortfolioView from '@/components/PortfolioView.vue'
import AboutComponentView from '@/components/AboutComponentView.vue'
import FooterView from '@/components/FooterView.vue'

export default defineComponent({
  name: 'HomeView',

  setup () {
    return {}
  },

  components: {
    NavBar,
    PortfolioView,
    AboutComponentView,
    FooterView
  }
})
</script>

<style scoped>

.v-container {
  padding: 16px 0 16px 0;
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

.first {
  whidt: 100%;
  text-align: center;
  padding: 2rem 2rem;
}
.imgHover {
  padding: 0 200px;
}

.pre {
  width: 100%;
  height: 380px;
  text-align: center;
  padding: 0 200px;
  background-color: #f5f5f5;
}

.hire {
  width: 100%;
  height: 200px;
  padding: 0 200px;
  background-color: #e9e9e9;
  margin-top: -24px;
}
</style>
