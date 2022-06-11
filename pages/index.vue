
<template>
  <div>
    <v-row justify="center">
      <v-img
        contain
        lazy-src="https://picsum.photos/id/11/10/6"
        max-height="300"
        max-width="500"
        src="https://picsum.photos/id/11/500/300"
        class="pa-1 ma-2"
      >
      </v-img>
    </v-row>
    <v-alert class="pa-1 ma-2 text-center">Hi! I'm Yuta! Wellcom to my portfolio page!</v-alert>
  </div>
</template>

<script>
  export default {
    name: 'IndexPage',
    data () {
      return {
        colors: [
          'primary',
          'secondary',
          'yellow darken-2',
          'red',
          'orange',
        ],
        model: 0,
      }
    },
    }
</script>