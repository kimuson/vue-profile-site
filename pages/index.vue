
<template>
  <div>
    <div id="hedderImg">
    <v-row justify="center" class="pa-1 ma-2">
      <v-img
        contain
        lazy-src="https://picsum.photos/id/11/10/6"
        max-height="300"
        max-width="500"
        src="https://picsum.photos/id/11/500/300"
      >
      </v-img>
    </v-row>
    </div>
    <div id="hedderMsg">
      <v-alert class="text-center">Hi! I'm Yuta! Wellcom to my portfolio page!</v-alert>
    </div>
    <div id="profileCard">
      <v-row justify="space-around" class="pa-5">
      <div>
        <h2 class="black--text">Yuta Kimura</h2>
        <p class="black--text">Software Engineer</p>
      </div>
      <div>
        <v-avatar size="111">
        <img
          src="https://pbs.twimg.com/profile_images/1402628898739789826/CBWMnKxq_400x400.jpg"
          alt="John"
          class="pa-1 ma-2">
        </v-avatar>
      </div>
      </v-row>
    </div>  
    <div id="WorkDisp" class="pa-1">
      <h3 class="black--text pa-1">Work</h3>
      <p class="black--text pa-1">His day job is as a data scientist. On the side, I am a private app developer.I manage a web media called "KIMURA LOG".</p>
      <v-row justify="center" class="pa-1 ma-2">
        <v-btn >
          My portfolio > 
        </v-btn>
      </v-row>
    </div>
    <div id="BioDisp" class="pa-1">
      <h3 class="black--text pa-1">Bio</h3>
      <p class="black--text pa-1">His day job is as a data scientist. On the side, I am a private app developer.I manage a web media called "KIMURA LOG".</p>
    </div>
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