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
        <p class="ma-3">
          ESET Smart Security Antivirus, a long-standing cyber security technology Protecting more than 110 million users worldwide, # 1 safety from the European Union, NOD32 technology has been the power of our products for more than 30 years, proven by continuous award winning. Complete online security Anti-malware solution for professional users. With the right balance of speed detection and usability, protect your digital identity with a long history of antivirus technology. Protect your kids online with ESET Parental control. Encrypts removable files and devices. Including managing and storing your passwords Protect your laptop with Anti-Theft.
        </p>
        <p class="ma-3">
          Download NOD32 Antivirus program. Small antivirus, easy to use, fast update. Does not consume resources. NOD32 is the most popular in Thailand of all time. Scan virus quickly and accurately ESET NOD32 Antivirus is a program that uses low system resources. It is suitable for all system environments and does not slow down your machine and has Gamer Mode to conserve system resources. Pop-ups, updates, and other resource-consuming activities will be postponed. If there is any program running in full screen, such as playing games, playing videos, or while projecting a presentation.
        </p>
      </v-main>
      <v-row dense class="px-3">
        <v-col
          v-for="(item, i) in items"
          :key="i"
          cols="12"
          class="mb-5 white lighten-1 "
        >
          <v-card class="pt-5">
          <v-img class="d-block d-sm-none mx-auto" width='150' :src="require('../assets/' + item.title + '.png')"></v-img>
            <div class="d-flex flex-no-wrap justify-start">
              <v-avatar
                class="ma-3 d-none d-sm-block"
                size="180"
                tile
              >
                <nuxt-link to="">
                  <v-img :src="require('../assets/' + item.title + '.png')"></v-img>
                </nuxt-link>
              </v-avatar>
              <div class="w-100">
                <v-card-title
                  class="headline mb-5"
                  v-text="item.title"
                ></v-card-title>

                <v-card-subtitle v-text="item.description"></v-card-subtitle>
                <v-card-actions>
                  <v-btn color='teal' class="mx-auto white-text">
                    <a :href="item.url" rel="noopener noreferrer">Download</a>
                  </v-btn>
                </v-card-actions>
              </div>
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
      items: [
        {
          src: 'https://cdn.vuetifyjs.com/images/cards/foster.jpg',
          title: 'ESET Smart Security Premium',
          description: 'The best of security solutions With multiple layers of protection and safety features Password encryption and management',
          url: 'https://download.eset.com/com/eset/tools/installers/live_essp/latest/eset_smart_security_premium_live_installer.exe'
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/cards/halcyon.png',
          title: 'ESET Internet Security',
          description: 'Advanced protection for a comprehensive daily internet experience.',
          url: 'https://download.eset.com/com/eset/tools/installers/live_eis/latest/eset_internet_security_live_installer.exe'
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/cards/foster.jpg',
          title: 'ESET NOD32 Antivirus',
          description: 'Antivirus standard For protection against hackers, malware and stealing your information. Without slowing down the machine',
          url: 'https://download.eset.com/com/eset/tools/installers/live_eav/latest/eset_nod32_antivirus_live_installer.exe'
        },
      ],
    }),
    methods:{
      download_file(){
        let target = document.getElementById('downL')
        target.attr({target: '_blank', 
                    href  : '../assets/sources/EIS_installer.exe'});
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
.v-card__subtitle{
  color: teal !important;
}
.v-application .headline{
  text-align: center !important;
  display: block !important;
  width: 100% !important;
  font-size: 1.5em !important;
  font-weight: bold;

  @media (max-width: 424px) {
    font-size: 1em !important;
  }
}

.v-card__actions{

  button{

    span{

      a{
        text-decoration: none;
        color: aliceblue;
      }
    }
  }
}
</style>

