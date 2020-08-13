<template>
  <v-card
    class="mx-auto"
  >
    <v-container class="pa-0">
      <v-main>
        <v-app-bar color="teal" dark>
          <v-toolbar-title class="mx-auto">
            <h1 class="ml-12">Install ESET NOD32</h1>
          </v-toolbar-title>
        </v-app-bar>
        <p class="ma-3">
          Before you begin the installation process Please close all open programs on your computer. ESET NOD32 Antivirus contains components that may conflict with other antivirus programs. Other antivirus programs that may already be installed on your computer. ESET recommends that you remove other antivirus programs. Out to prevent any problems that may arise. You can install ESET NOD32 Antivirus from the installation CD or from the files provided on the ESET website.
        </p>
        <p class="ma-3">
          *** If there is a third-party antivirus program on your computer Please uninstall the program before following the installation steps.
        </p>
        <ol class="ml-5 mb-5">
          <li>Installation procedure for virus scan program Download antivirus nod32 from the official website <a target="_blank" href="https://www.eset.com/us/home/free-trial">www.eset.com</a> or <nuxt-link to="/download">click here</nuxt-link></li>
          <li> Double click the downloaded file live_installer.exe and press OK.</li>
          <li>Select the language of the program and press the Continue button (as shown below).</li>
        </ol>
      </v-main>
      <v-row dense class="px-3">
        <v-col
          v-for="(item, i) in 9"
          :key="i"
          cols="12"
          class="mb-5 white lighten-1 "
        >
          <v-card>
            <div class="d-flex flex-no-wrap justify-start">
              <v-avatar
                class="ma-3 mx-auto w-100"
                tile
                height='100%'
              >
                  <v-img class="" :src="require('../assets/install/' +[i+1] + '.png')"></v-img>
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
      
    }),
    methods:{
    
    },
    head(){
      return{
        title: 'Serial Depot | Install'
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

