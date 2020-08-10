<template>
  <v-card>
    <v-footer
      padless
    >
      <v-card
        flat
        tile
        width="100%"
        class="lighten-1 text-center"
      >
        <v-card-text>
         <v-bottom-navigation
            grow
            color="yellow"
        >
            <v-btn><nuxt-link to="/">Home</nuxt-link></v-btn>
            <v-btn><nuxt-link to="/download">Download</nuxt-link></v-btn>
            <v-btn><nuxt-link to="/install">Install</nuxt-link></v-btn>
            <v-btn><nuxt-link to="/install">Activate</nuxt-link></v-btn>
            <v-btn><nuxt-link to="/install">About</nuxt-link></v-btn>
            <v-btn><nuxt-link to="/install">Contact</nuxt-link></v-btn>
        </v-bottom-navigation>
        </v-card-text>

        <v-divider></v-divider>

        <v-card-text class="white--text">
         <strong><nuxt-link class="white--text" to="/">Serial Depot</nuxt-link></strong> {{ new Date().getFullYear()}}
        </v-card-text>
      </v-card>
    </v-footer>
  </v-card>
</template>

<script>
  export default {
    data: () => ({
      icons: [
        'mdi-home',
        'mdi-email',
        'mdi-calendar',
        'mdi-delete',
      ],
      items: [
        'default',
        'absolute',
        'fixed',
      ],
      padless: false,
      variant: 'default',
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

            a{
                color: aliceblue;
                text-decoration: none;
            }
        }
    }
}
</style>
