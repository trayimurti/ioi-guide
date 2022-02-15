<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      fixed
      temporary
    >
      <v-list shaped>
        <v-subheader>Sections</v-subheader>
        <v-list-item-group>
          <NuxtLink class="navLink" to="/zonal">
          <v-list-item link>
              <v-list-item-content>
                <v-list-item-title>Zonal</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </NuxtLink>
          <NuxtLink class="navLink" to="/national">
          <v-list-item link>
              <v-list-item-content>
                <v-list-item-title>National</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </NuxtLink>
          <NuxtLink class="navLink" to="/training-camp">
          <v-list-item link>
              <v-list-item-content>
                <v-list-item-title>Training Camp</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </NuxtLink>
          <NuxtLink class="navLink" to="/international">
          <v-list-item link>
              <v-list-item-content>
                <v-list-item-title>International</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </NuxtLink>
        </v-list-item-group>
      </v-list>

      <v-divider></v-divider>

      <v-list shaped>
        <v-subheader>Problems</v-subheader>
        <v-list-item-group>
          <NuxtLink class="navLink" to="/problems">
          <v-list-item link>
              <v-list-item-content>
                <v-list-item-title>Problems</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </NuxtLink>
        </v-list-item-group>
      </v-list>

      <v-divider></v-divider>

      <v-list shaped>
        <v-subheader>Archive</v-subheader>
        <v-list-item-group>
          <NuxtLink class="navLink" to="/archive/zio">
          <v-list-item link>
              <v-list-item-content>
                <v-list-item-title>ZIO</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </NuxtLink>
          <NuxtLink class="navLink" to="/archive/zco">
          <v-list-item link>
              <v-list-item-content>
                <v-list-item-title>ZCO</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </NuxtLink>
          <NuxtLink class="navLink" to="/archive/inoi">
          <v-list-item link>
              <v-list-item-content>
                <v-list-item-title>INOI</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </NuxtLink>
          <NuxtLink class="navLink" to="/archive/ioitc">
          <v-list-item link>
              <v-list-item-content>
                <v-list-item-title>IOITC</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </NuxtLink>
          <NuxtLink class="navLink" to="/archive/ioi">
          <v-list-item link>
              <v-list-item-content>
                <v-list-item-title>IOI</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </NuxtLink>
        </v-list-item-group>
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

      <NuxtLink class="navLink" to="/">
        <v-img src="logo.png"  height="55" max-width="60" style="margin-right: 10px;"></v-img>
      </NuxtLink>

      <v-spacer></v-spacer>

      <v-btn class="nav-link" icon
      @click.stop="$nuxt.$vuetify.theme.isDark = !$nuxt.$vuetify.theme.isDark">
        <v-icon>mdi-theme-light-dark</v-icon>
      </v-btn>

      <v-btn class="nav-link" icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main class="main" dark>
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

.main{
  width:100%;
  height:100%;
}

.navLink{
  text-decoration:none;
  color: #43c293;
}
</style>