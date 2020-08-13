<template>
  <v-card
    class="mx-auto"
  >
    <v-container class="pa-0">
      <v-main>
        <v-app-bar color="teal" dark>
          <v-toolbar-title class="mx-auto">
            <h1 class="ml-12">Download ESET NOD32</h1>
          </v-toolbar-title>
        </v-app-bar>
        <p class="ma-3">Activate or Register ESET Products Today is a guide to how to Activate Nod32 Antivirus easily. That anyone can do as described below</p>
        <p class="ma-3">
          For anyone who is looking for a genuine antivirus program I said before that the program ESET camps cannot Activate Nod32 or Crack Nod32 for life. You must only find the key. And today I have gathered together the keys for free. I will keep updating when new keys come in. For people who need keys You can get the keys from <nuxt-link to="/">here</nuxt-link>
        </p>
      </v-main>
      <v-row dense class="px-3">
          <div class=" d-flex flex-column">
            <b class="mt-5 mb-2"></b>
            <b class="mt-5 mb-2"></b>
          </div>
        <v-col
          v-for="(item, i) in decsription"
          :key="i"
          cols="12"
          class="mb-5 white lighten-1 "
        >
          <v-card>
               <p class="pa-3"><b>{{item}}</b></p>
            <div class="d-flex flex-no-wrap justify-start">
              <v-avatar
                class="ma-3 mx-auto w-100"
                tile
                height='100%'
              >
                  <v-img class="" :src="require('../assets/activate/' +[i+1] + '.png')"></v-img>
              </v-avatar>
            </div>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
</template>

<script>
  export default {
    data: () => ({
      decsription:[
        '1. Launch ESET program and click on the Help and Support topic.', 
        '2. Look below the right hand will have the word (change license), click it.',
        '3. Select the subject, use the license code purchased.',
        '4. Please enter the Key Nod32 obtained from this website in the License key field, then click Continue.',
        '5. Press Activate.',
        '6. That\'s it, activation completed successfully. You will be able now to use the program Nod32.'
      ]
    }),
    methods:{
    
    },
    head(){
      return{
        title: 'Serial Depot | Activate'
      }
    } 
  }
</script>

<style lang="scss">
h1{
  font-size: 2em;

  @media (max-width: 400px) {
    font-size: 0.8em;
  }

  @media (min-width: 401px) and (max-width: 600px) {
    font-size: 1.25em;
  }
}

</style>

