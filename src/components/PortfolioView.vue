<template>
        <div class="first" id="project">
          <v-row>
            <v-col>
              <div class="child mx-auto my-auto text-center">
                <v-img height="5em" src="../assets/icon/software-development.png"/>
                <h3 class="ml-3 mt-4">Web Developer</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Progetti creati come Web Developer
                </p>
              </div>
              <v-row align="center" justify="center" >
                <template v-for="(item, i) in visibleItems" :key="i" >
                  <v-col cols="12" md="4">
                    <v-hover v-slot="isHovering, props" >
                      <a :href="item.link" target="_blank" rel="noopener noreferrer" style="text-decoration: none; color: inherit;">
                      <v-card :elevation="isHovering ? 12 : 2" :class="{ 'on-hover': isHovering }" v-bind="props">
                        <v-img :src="item.img" height="225" cover></v-img>
                        <v-card-title>{{item.title}}</v-card-title>
                        <v-card-subtitle>
                          {{ item.tecnologie }}
                        </v-card-subtitle>
                        <v-card-text>
                          {{ item.description }}
                        </v-card-text>
                        <!-- {{ console.log('Rendering card:', item) }} -->
                      </v-card>
                    </a>
                    </v-hover>
                  </v-col>
                </template>
            </v-row>

          <v-col cols="12" sm="12">
              <div class="d-flex justify-center mb-6">
                <v-btn color="blue" class="mt-4" @click="loadMore">
                  load more
                </v-btn>
              </div>
            </v-col>

            </v-col>

          </v-row>
  </div>

</template>

<script>

import { ref } from 'vue'

export default {
  setup () {
    const itemsToShow = ref(6)
    return {
      items: [
        {
          img: require('@/assets/Netflox.png'),
          link: 'https://bluealastor.github.io/netflox/',
          title: 'Netflox',
          description: 'Primo progetto clone Netflix',
          tecnologie: 'Html, Css, Javascript'
        },
        {
          img: require('@/assets/Amaca Travel.png'),
          link: 'https://github.com/ilPhil/amaca-travel',
          title: 'Amaca Travel',
          description: 'Progetto finale di edgemony',
          tecnologie: 'NEXT.js, Css, Javascript'
        },
        {
          img: require('@/assets/CocktailDB.png'),
          link: 'https://thecocktaildb-angular-v17.vercel.app/detail/14456',
          title: 'CocktailDB',
          description: 'Progetto con Angular 17',
          tecnologie: 'Angular 17, Css, Typescript, Bootstrap'
        },
        {
          img: require('@/assets/Pokedex.png'),
          link: 'https://main--fantastic-rabanadas-dc8b5c.netlify.app/',
          title: 'Pokedex',
          description: 'Progetto con React,js',
          tecnologie: 'React.js, Css, Javascript'
        }
      ],
      itemsToShow
    }
  },
  computed: {
    visibleItems () {
      return this.items.slice(0, this.itemsToShow)
    },
    shouldShowLoadMore () {
      return this.itemsToShow < this.items.length
    }
  },
  methods: {
    loadMore () {
      this.itemsToShow += 20
      // console.log('Load more clicked, itemsToShow:', this.itemsToShow)
    }
  }
}
</script>

<style scoped>
.first {
  whidt: 100%;
  text-align: center;
  padding: 2rem 2rem;
}

.child {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: center;
  margin-right: 8px;
}
</style>
