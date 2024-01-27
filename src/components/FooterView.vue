<template>
    <v-footer>
      <v-card elevation="0" rounded="0" width="100vw" class="text-center" color="#FAFAFA">
          <v-card-text>
              <v-btn class="mx-4" variant="text" @click="scroll('portfolio')">Portfolio</v-btn>
              <v-btn class="mx-4" variant="text" @click="scroll('home')">Home</v-btn>
              <v-btn class="mx-4" variant="text" @click="scroll('about')" >About us</v-btn>
              <v-btn class="mx-4" variant="text" :href="'mailto:' + 'chrisexp00@gmail.com'">Contact</v-btn>
          </v-card-text>
          <v-card-text>
              @ {{ new Date().getFullYear()}} <strong></strong>
          </v-card-text>
      </v-card>
    </v-footer>
  </template>

<script>
export default {
  methods: {
    scroll (refName) {
      const element = document.getElementById(refName)
      element.scrollIntoView({ behavior: 'smooth' })
    }
  }

}
</script>

  <style scoped>
  .v-footer {
    padding: 8px 0 !important;
  }

  a{
    text-decoration: none;
  }
  </style>
