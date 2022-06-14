<template>
  <v-app :dark="setTheme">
    <v-app-bar
      :collapse="!collapseOnScroll"
      :collapse-on-scroll="collapseOnScroll"
      absolute
      dark
      scroll-target="#scrolling-techniques-6"
    >
    
      <v-toolbar-title>Yuta Kimura</v-toolbar-title>
      <div class="pl-2">
        <v-btn text>WORK</v-btn>
        <v-btn text>POST</v-btn>
        <v-btn text href="https://github.com/kimuson"><fa :icon="['fab', 'fa-github']" />&nbsp;SOURCE</v-btn>
      </div>
      <v-spacer></v-spacer>
      <template v-if="goDark">
        <v-btn text @click="changeThema()">
        <fa :icon="['fas', 'fa-sun']" />
        </v-btn>
      </template>
      <template v-else>
        <v-btn text @click="changeThema()">
        <fa :icon="['fas', 'fa-moon']" />
        </v-btn>
      </template>
    </v-app-bar>
    <v-spacer></v-spacer>
    <v-main class="grey lighten-3">
      <v-container>
        <v-row>
          <v-col
            cols="12"
            sm="2"
          >
          </v-col>

          <v-col
            cols="12"
            sm="8"
          >
            <Nuxt />
          </v-col>
          <v-col
            cols="12"
            sm="2"
          >
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>

  export default {
    name: 'DefaultLayout',
    data: () => ({
      goDark: false,
      links: [
        'Profile',
        'Works',
        'Posts',
        'Source',
      ],
      collapseOnScroll: true,
      title: 'Yuta Kimura',
    }),
    methods: {
    changeThema: function() {
        console.log('AAAAAAAAAAAAAAAAAAAAA');
        console.log(this.goDark);
        this.goDark=!this.goDark
    }
  },
    computed: {
        setTheme() {
            if (this.goDark == true) {
                return (this.$vuetify.theme.dark = true);
            } else {
                return (this.$vuetify.theme.dark = false);
            }
        }
    }
  }
</script>
