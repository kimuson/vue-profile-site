
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
      <u><h3 class="black--text">Work.</h3></u>
      <p class="black--text pa-1">His day job is as a data scientist. On the side, I am a private app developer.I manage a web media called "KIMURA LOG".</p>
      <v-row justify="center" class="pa-1 ma-2">
        <v-btn >
          <a class="white--text" href="https://kimuralog.com/?p=60" target=”_blank”>My portfolio ></a>
        </v-btn>
      </v-row>
    </div>
    <div id="BioDisp" class="pb-2">
      <u><h3 class="black--text pb-4">Bio.</h3></u>
       <v-row class="pl-2 pb-0">
         <b class="black--text pl-5 pb-0">2014</b>
         <p class="black--text pl-5 pb-0">Serverside Engineer/HR industry</p>
       </v-row>
       <v-row class="pl-2">
         <b class="black--text pl-5 pb-0">2018</b>
         <p class="black--text pl-5 pb-0">IT director/HR industry</p>
       </v-row>
       <v-row class="pl-2">
         <b class="black--text pl-5 pb-0">2020</b>
         <p class="black--text pl-5 pb-0">Data Engineer/Payment industry</p>
       </v-row>
    </div>
    <div id="InterestsDisp" class="pa-1">
      <u><h3 class="black--text">Interests.</h3></u>
      <p class="black--text pa-1">Mathematics,Tennis,Machine learning,history of mankind</p>
    </div>
    <div id="MediaDisp" class="pa-1">
      <u><h3 class="black--text pb-4">Media.</h3></u>
       <v-row class="pl-2 pb-0">
         <p class="black--text pl-5 pb-0">
           <v-btn text href="https://github.com/kimuson"><fa :icon="['fab', 'fa-github']" />&nbsp;@kimuson</v-btn>
           <v-btn text href="https://twitter.com/kimura9438"><fa :icon="['fab', 'fa-twitter']" />&nbsp;@kimura9438</v-btn>
           <v-btn text href="https://bit.ly/3xqHx5n"><fa :icon="['fas', 'fa-blog']" />&nbsp;kimuralog.com</v-btn>
           </p>
       </v-row>
       
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