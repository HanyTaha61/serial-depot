<template>
  <v-app>
    <v-card class="w-100">
      <v-app-bar color="teal" dark>
        <v-toolbar-title class="mx-auto">
          <h1 class="ml-12">Contact Us</h1>
        </v-toolbar-title>
      </v-app-bar>
    </v-card>
    <img class="d-block w-75" src="../assets/contact.jpg" alt="">
    <div class="about_ESET pa-2 mt-3">
      <p class="mt-10">
          you can contact me via :
        <ol>
            <li>
                <a class="d-block w-fit" target="_blank" href="mailto:hanygrand1980@gmail.com"><img class="d-block my-2" width="48" src="../assets/gmail.png" alt="mail"></a>
            </li>
            <li>
                <a class="d-block w-fit" target="_blank" href="https://www.facebook.com/messages/t/hany.loverw"><img class="d-block my-2" width="48" src="../assets/facebook.png" alt="fb"></a>
            </li>
        </ol>
      </p>
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
      title: 'Serial Depot | Contact Us'
    }
  }
}
</script>

<style lang='scss' scoped>

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
      .about_ESET{

          ol{
              padding-top: 30px !important;

              li{
                    margin-bottom: 20px;

                    a{
                        position: relative;
                        top: -7px
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
