<template>
  <v-img
    :src="require('@/assets/background-1.jpg')"
    gradient="to top right, rgba(101,78,163,.85), rgba(255,121,19,.65)"
    height="75vh"
    position="left center"
  >
    <v-container fill-height>
      <v-layout align-center>
        <v-flex text-xs-center white--text shadowed-text>
          <v-avatar :size="150">
            <img
              class="rotate-15d"
              :src="require('@/assets/sonny-avatar.png')"
              alt="avatar"
            />
          </v-avatar>
          <h1 class="display-2 font-weight-bold text-uppercase mb-3">
            {{ name }}
          </h1>
          <div class="title font-weight-light text-uppercase mb-2">
            {{ function_ }}
          </div>
          <div class="caption text-uppercase">{{ experience_level }}</div>
        </v-flex>
      </v-layout>
    </v-container>
  </v-img>
</template>

<script>
export default {
  data: () => ({
    name: 'Sonny',
    function_: 'Software Developer',
    experience_level: 'Senior'
  })
}
</script>

<style scoped>
img.rotate-15d {
  transform: rotate(15deg);
}
</style>
