<template>
  <v-card>
    <v-footer
      padless
    >
          <v-container>
      <v-card
        flat
        tile
        width="100%"
        class="lighten-1 text-center"
      >
        <v-card-text class="d-none d-sm-block">
         <v-bottom-navigation
        
            grow
            color=""
        >
              <v-btn class="px-0"><nuxt-link exact to="/">Home</nuxt-link></v-btn>
              <v-btn class="px-0"><nuxt-link to="/download">Download</nuxt-link></v-btn>
              <v-btn class="px-0"><nuxt-link to="/install">Install</nuxt-link></v-btn>
              <v-btn class="px-0"><nuxt-link to="/activate">Activate</nuxt-link></v-btn>
              <v-btn class="px-0"><nuxt-link to="/about">About</nuxt-link></v-btn>
              <v-btn class="px-0"><nuxt-link to="/contact">Contact</nuxt-link></v-btn>
        </v-bottom-navigation>
        </v-card-text>

        <v-divider class="d-none d-sm-block"></v-divider>

        <v-card-text class="white--text">
         <strong><nuxt-link class="white--text" to="/">Serial Depot</nuxt-link></strong> {{ new Date().getFullYear()}}
        </v-card-text>
      </v-card>
          </v-container>
    </v-footer>
  </v-card>
</template>

<script>
  export default {
    data: () => ({

    }),
    computed: {
      localAttrs () {
        const attrs = {}

        if (this.variant === 'default') {
          attrs.absolute = false
          attrs.fixed = false
        } else {
          attrs[this.variant] = true
        }
        return attrs
      },
    },
  }
</script>

<style lang="scss" scoped>
strong a{
    text-decoration: none;
}
.theme--dark.v-footer{
    background-color: #0096a9 !important;
}
.v-bottom-navigation{

    button{

        span{

            a, a.nuxt-link-exact-active{
                color: aliceblue;
                text-decoration: none;
                width: 100%;
                height: 100%;
                line-height: 4.5 !important;
            }
            a.nuxt-link-exact-active{
              background-color: #eee;
              color: teal;
            }
        }
    }
}
</style>
