<template>
  <v-app>
    <v-card class="w-100">
      <v-app-bar color="teal" dark>
        <v-toolbar-title class="mx-auto">
          <h1 class="ml-12">About Us</h1>
        </v-toolbar-title>
      </v-app-bar>
      <v-img :src= "require('assets/about.png')" class="my-5"></v-img>
    </v-card>
    <div class="about_ESET pa-2 mt-3">
      Our website is another great way to recommend software or programs that you should use for virus scanners. Also known as ESET NOD32 Antivirus or shortened by name. That NOD32 is a Shareware program from the ESET developer camp who developed this virus scanner.
      <p class="mt-10">
        Which our website has recommended Stages of use reviews Customization Various installations Including a way to download and use to use This download is a trial version. That can be used for free for 30 days (Trial Version) by the program developers agree to be published. Program recommended And our website is not involved in the distribution of any illegal or infringing programs.
      </p>
      <p class="mt-10">For which users Anyone who already uses ESET NOD32 Antivirus and likes it in the program. You can contact the developer to purchase the full version. By contacting us at:</p>
      <p><b>
        ESET Middle East<br>
        Office no. 110, E Block, Office Park Building<br>
        Dubai Internet City<br>
        Dubai<br>
        United Arab Emirates<br>
        Email: service@esetme.com<br>
        Web: www.eset.com/me/
      </b></p>
    </div>
  </v-app>
</template>

<script>
export default {
  data(){
    return{
      }
  },
  head(){
    return{
      title: 'Serial Depot | About Us'
    }
  }
}
</script>

<style lang='scss'>

body{
	font-family: 'Montserrat', sans-serif;
}

.theme--dark.v-application, .theme--dark.v-card{
  background-color: unset !important;
  color: unset;
}

.v-application--wrap{
 
  .v-toolbar__content{
    background-color: #0096a1;

    .v-toolbar__title{

      h1{
        font-size: 2em;

        @media (max-width: 400px) {
          font-size: 0.8em;
        }

        @media (min-width: 401px) and (max-width: 600px) {
          font-size: 1.25em;
        }
      }
    }
  }
}

.w-100{
  width: 100% !important
}
.w-fit{
  width: fit-content !important;
}
body{
  background-color: #eee;
}
.border{
  border: 1px solid #ccc;
}
.mx-auto{
  display: block !important;
  margin-left: auto !important;
  margin-right: auto !important;
}
</style>
