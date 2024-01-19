<template>
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
              <CardComponent/>
              <!-- <div class="child">
                <v-btn icon="fas fa-camera" color="blue" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">Fotografia</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                 Di seguito alcuni miei Scatti come Fotografo
                </p>
             </div> -->
            </v-col>

          </v-row>

        </div>

</template>

<script>
import CardComponent from './CardComponent.vue'

export default {
  components: { CardComponent }
}
</script>

<style scoped>

</style>
