<template>
  <v-app>
    <v-navigation-drawer
        v-model="drawer"
        fixed
        temporary
        right
    >
      <v-list class="pa-1">
        <v-list-tile>
          <v-img
            :src="require('@/assets/logo-softllama-right-text.png')"
            class="my-3 clickable"
            contain
            height="50"
            @click="$vuetify.goTo(0)"
          ></v-img>
        </v-list-tile>
      </v-list>

      <v-list class="pt-0" dense>
        <v-divider></v-divider>

        <v-list-tile
          v-for="item in items"
          :key="item.title"
          @click="$vuetify.goTo('#'+item.title.toLowerCase())"
        >
          <v-list-tile-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-tile-action>

          <v-list-tile-content>
            <v-list-tile-title>{{ item.title }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar app>
      <v-toolbar-title
        class="headline text-uppercase clickable"
        @click="$vuetify.goTo(0)"
      >
        <span>{{ title }}</span>
        <span class="font-weight-light">{{ subtitle }}</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-menu class="hidden-md-and-up">
        <v-toolbar-side-icon
          slot="activator"
          @click.stop="drawer = !drawer"
        >
        </v-toolbar-side-icon>
      </v-menu>
      <v-toolbar-items v-for="item in items" :key="item.title" class="hidden-sm-and-down">
        <v-btn flat @click="$vuetify.goTo('#'+item.title.toLowerCase())">
          <span class="mr-2">{{ item.title }}</span>
          <v-icon>{{ item.icon }}</v-icon>
        </v-btn>
      </v-toolbar-items>
    </v-toolbar>
    <v-content>
      <router-view/>
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data: () => ({
    title: 'softllama',
    subtitle: 'homepage',
    drawer: null,
    items: [
      { title: 'About', icon: 'person' },
      { title: 'Skills', icon: 'keyboard' }
    ]
  })
}
</script>

<style>
.clickable {
  cursor: pointer;
}
.section-layout:nth-child(odd) {
  background: rgba(101,78,163,.05);
}
</style>
