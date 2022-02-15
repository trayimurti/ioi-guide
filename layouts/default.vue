<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      absolute
    >
      <v-list shaped>
        <v-subheader>Sections</v-subheader>
        <v-list-item-group>
          <v-list-item link>
            <v-list-item-content>
              <v-list-item-title>ZIO</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link>
            <v-list-item-content>
              <v-list-item-title>ZCO</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link>
            <v-list-item-content>
              <v-list-item-title>INOI</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link>
            <v-list-item-content>
              <v-list-item-title>IOITC</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link>
            <v-list-item-content>
              <v-list-item-title>IOI</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>

      <v-divider></v-divider>

      <v-list shaped>
        <v-list-item link>
          <v-list-item-title>Problems</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      absolute
      elevate-on-scroll
      scroll-target="#scrolling-techniques-7"
    >
      <v-app-bar-nav-icon
      @click.stop="drawer = !drawer">
      </v-app-bar-nav-icon>

      <v-btn href="https://github.com/trayimurti/ioi-guide" icon>
        <v-icon>mdi-github</v-icon>
      </v-btn>

      <v-spacer></v-spacer>

      <v-img src="logo.png"  height="35" max-width="40" style="margin-right: 10px;"></v-img>
      <v-toolbar-title> IOI Guide</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn class="nav-link" icon
      @click.stop="$nuxt.$vuetify.theme.isDark = !$nuxt.$vuetify.theme.isDark">
        <v-icon>mdi-theme-light-dark</v-icon>
      </v-btn>

      <v-btn class="nav-link" icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main style="margin-top:80px;" dark>
      <v-container dark>
        <nuxt dark/>
      </v-container>
    </v-main>

    <v-footer>

      <v-divider></v-divider>
      
      <v-img src="logo.png" max-height="50" max-width="60"></v-img>
      <v-divider></v-divider>

      <v-col
        class="text-center"
        cols="12"
      >
        {{ new Date().getFullYear() }} — <strong>IOI Guide</strong>
      </v-col>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      drawer: false,

    }
  }
}
</script>

<style scoped>
.nav-link{
  margin: 0 5px;
}
</style>