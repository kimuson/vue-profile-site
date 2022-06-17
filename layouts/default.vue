<template>
  <v-app>

    <v-app-bar
      :collapse="!collapseOnScroll"
      :collapse-on-scroll="collapseOnScroll"
      absolute
      dark app
      scroll-target="#scrolling-techniques-6"
    >
    <v-app-bar-nav-icon @click="drawer = true" v-if="$vuetify.breakpoint.xs"></v-app-bar-nav-icon>
      <v-toolbar-title><nuxt-link to="/" class="c-p" tag="div">Yuta Kimura</nuxt-link></v-toolbar-title>
      <div class="pl-2">
        <v-btn text v-if="!$vuetify.breakpoint.xs" to="/work" nuxt>WORK</v-btn>
        <v-btn text v-if="!$vuetify.breakpoint.xs" to="/post" post>POST</v-btn>
        <v-btn text href="https://github.com/kimuson" v-if="!$vuetify.breakpoint.xs"><fa :icon="['fab', 'fa-github']" />&nbsp;SOURCE</v-btn>
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
     <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
    >
      <v-list
        nav
        dense
      >
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-title><nuxt-link to="work" class="c-p" tag="div">WORK</nuxt-link></v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title><nuxt-link to="post" class="c-p" tag="div">POST</nuxt-link></v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title ><a href="https://github.com/kimuson" style="cursor:default;color:inherit;text-decoration:none;">SOURCE</a></v-list-item-title>
          </v-list-item>
          
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <v-main>
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
      <v-footer padless>
    <v-col
      class="text-center"
      cols="12"
    >
      {{ new Date().getFullYear() }} — <strong>Create by Yuta Kimura</strong>
    </v-col>
  </v-footer>
  </v-app>
</template>

<script>

  export default {
    name: 'DefaultLayout',
    data: () => ({
      drawer: false,
      group: null,
      goDark: true,
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
    },
    watch: {
    goDark() {
      this.$vuetify.theme.dark = this.goDark
    }
  },
    
  }
</script>
<style>
.c-p {
  cursor: pointer;
}
</style>