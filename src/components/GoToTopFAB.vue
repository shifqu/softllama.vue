<template>
  <v-fab-transition>
    <v-btn
      v-show="fab"
      v-scroll="onScroll"
      fab
      fixed
      bottom
      right
      color="primary"
      @click="toTop"
    >
      <v-icon>keyboard_arrow_up</v-icon>
    </v-btn>
  </v-fab-transition>
</template>

<script>
export default {
  name: 'AppFab',
  data: () => ({
    fab: false
  }),
  methods: {
    onScroll () {
      if (typeof window === 'undefined') return
      const top = window.pageYOffset || document.documentElement.offsetTop || 0
      this.fab = top > 300
    },
    toTop () {
      this.$router.push({ hash: '' })
      this.$vuetify.goTo(0)
    }
  }
}
</script>
