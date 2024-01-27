<template>
    <v-app-bar app color="black" dark flat class="px-12">
        <v-btn>
            <v-icon color="blue" left class="mr-2">fas fa-user-tie</v-icon>Christian
        </v-btn>
        <v-spacer></v-spacer>
      <a @click="scroll('home')" class=" link">Home</a>
      <a @click="scroll('about')" class=" link">About</a>
      <a @click="scroll('portfolio')" class=" link">Portfolio</a>
      <a :href="'mailto:' + 'chrisexp00@gmail.com' " class=" link">Contact</a>
        <!-- <v-btn @click="scroll('home')" class="link">Home</v-btn>
        <v-btn @click="scroll('about')" class="link">About</v-btn>
        <v-btn @click="scroll('portfolio')" class="link">Portfolio</v-btn>
        <v-btn @click="scroll('contact')" class="link">Contact</v-btn> -->

    </v-app-bar>
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
*{
    margin: 0;
}

a{
  text-decoration: none;
}
.link{
  color: #ffffff;
  padding: 1rem 2rem;
  position: relative;
}

.link::before,
.link::after {
  content: "";
  position: absolute;
  width: 100%;
  height: 2px;
  background: blue;
  transform:  scaleX(0);
  transition: all 1s ease;
}
.link::before{
  top: 0;
  left: 0;
  transform-origin: left;
}

.link::after{
  bottom: 0;
  left: 0;
  transform-origin: right ;
}

.link:hover::before,
.link:hover::after{
  transform: scaleX(1);
}
</style>
