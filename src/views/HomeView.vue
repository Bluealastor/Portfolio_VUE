<template>
  <v-app id="home">
    <NavBar/>
    <v-container fluid>
      <div class="head">
        <v-row>
        <v-col cols="5">
          <div class="container-text mt-16">
            <h2 class="text-white">Hello,</h2>
            <h2 class="text-white">I'M Chrstian Esposito</h2>
            <span class="text-white">Web Developer</span><br />
            <v-btn tile dark class="text-blue mt-8" variant="outlined">Contact Me</v-btn>
          </div>
        </v-col>
        <v-col cols="2">
          <div style="position:absolute; z-index:9999; bottom:0; margin-left:auto; margin-right:auto; left:0; right:0; text-align:center">
            <v-icon>fas fa-angle-double-down</v-icon>
          </div>
        </v-col>
        <v-col cols="5">
          <div style="position:relative; z-index: 9999;" class="mt-16">
            <v-img src="https://kgrassociates.com/wp-content/uploads/sites/36/2016/06/Happy-Business-Guy.jpg" contain max-height="300"></v-img>
          </div>
        </v-col>
        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="6">
              <div class="egg">
                <v-img src="https://kgrassociates.com/wp-content/uploads/sites/36/2016/06/Happy-Business-Guy.jpg" max-height="300"></v-img>
              </div>
            </v-col>
          </v-row>
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
.v-container{
  padding: 16px 0;
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

.head:before{
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  height:100%;
  width:50%;
  background-color: black;
  transform: skew(0deg, 3deg);
}

.head:after{
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  height:100%;
  width:50%;
  background-color: black;
  transform: skew(0deg, 6deg);
}

.container-text{
  position: relative;
}

.egg{
  display: block;
  margin-left: 100px;
  margin-top: 50px;
  width: 356px;
  height: 300px;
  background-color: #FBDF7F;
  border-radius:50% 50% 50% 50%  / 60% 60% 40%;
}

</style>
