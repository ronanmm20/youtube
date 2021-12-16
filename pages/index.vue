<template>
<div>
    <v-sheet
    class="mx-auto mb-2"
  >
    <v-slide-group
      show-arrows
    >
      <v-slide-item
        v-for="n in 25"
        :key="n"
        v-slot="{ active, toggle }"
        class="mt-"
      >
        <v-btn
          class="mx-2"
          :input-value="active"
          active-class="white--text"
          depressed
          rounded
          @click="toggle"
        >
          {{ keywords[n] }}
        </v-btn>
      </v-slide-item>
    </v-slide-group>
  </v-sheet>

    <v-row no-gutters>
      <v-card
        v-for="n in 3"
        :key="n"
        class="pl-1 mx-5 my-2"
        
      >
      <v-responsive
          v-if="n === 2"
          :key="`width-${n}`"
          width="100%" 
        ></v-responsive>
    <v-img class="py-1"
      src="https://i1.sndcdn.com/artworks-bXANGgDMELEJkNOM-ZqRY1g-t500x500.jpg"
      height="230px"
      width="250px"
    ></v-img>

    <v-card-title class="py-4">
      exeter <v-icon>mdi-dots-vertical</v-icon>
    </v-card-title>

    <v-card-subtitle class="pa-0">
      drain gang <v-icon>mdi-check-decagram</v-icon>
    </v-card-subtitle>

    <v-card-subtitle class="pa-0">
      583k views 5 days ago
    </v-card-subtitle>
    </v-card>
    </v-row>





    <v-row no-gutters>
      <v-card
        v-for="n in 3"
        :key="n"
        class="pl-1 mx-5 my-2"
      >
      <v-responsive
          v-if="n === 2"
          :key="`width-${n}`"
          width="100%" 
        ></v-responsive>
    <v-img class="py-2"
      src="https://preview.redd.it/oax5lic6ny161.png?auto=webp&s=b95cb6da34a2aba03944c9e62b931713e0dd6677"
      height="230px"
      width="250px"
    ></v-img>

    <v-card-title class="py-4">
      333 <v-icon>mdi-dots-vertical</v-icon>
    </v-card-title>

    <v-card-subtitle class="pa-0">
      drain gang <v-icon>mdi-check-decagram</v-icon>
    </v-card-subtitle>

    <v-card-subtitle class="pa-0">
      362k views 11 hour ago
    </v-card-subtitle>
    </v-card>
    </v-row>

    <v-row no-gutters>
      <v-card
        v-for="n in 3"
        :key="n"
        class="pl-1 mx-5 my-2"
      >
      <v-responsive
          v-if="n === 2"
          :key="`width-${n}`"
          width="100%" 
        ></v-responsive>
    <v-img class="py-2"
      src="https://img.youtube.com/vi/sNuMM_9UqZU/0.jpg"
      height="230px"
      width="250px"
    ></v-img>

    <v-card-title class="py-4">
      gluee <v-icon>mdi-dots-vertical</v-icon>
    </v-card-title>

    <v-card-subtitle class="pa-0">
      drain gang <v-icon>mdi-check-decagram</v-icon>
    </v-card-subtitle>

    <v-card-subtitle class="pa-0">
      2M views 28 days ago
    </v-card-subtitle>
    </v-card>
    </v-row>

</div>
</template>
<script>

export default {
  data: () => ({
    keywords: ['Music', 'Mixes', 'Laughter', 'COVID', 'Programming', 'League of Legends', 'Cryptocurrency', 'Rap', 'Paintball', 'Marvel', 'Tesla', 'Trailers', 'Reaction videos', 'Experiments', 'Outer space', 'Aliens'],
  }),
}
</script>

