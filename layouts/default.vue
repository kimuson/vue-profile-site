<template>
  <v-app dark>
    <v-app-bar
      :collapse="!collapseOnScroll"
      :collapse-on-scroll="collapseOnScroll"
      absolute
      dark
      scroll-target="#scrolling-techniques-6"
    >
      

      <v-toolbar-title> Yuta Kimura</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-checkbox
        v-model="collapseOnScroll"
        color="white"
        hide-details
      ></v-checkbox>
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
      links: [
        'Profile',
        'Works',
        'Posts',
        'Source',
      ],
      collapseOnScroll: true,
      title: 'Yuta Kimura',
    }),
  }
</script>
