<template>
  <v-img
    :src="require('@/assets/background-1.jpg')"
    gradient="to top right, rgba(101,78,163,.85), rgba(255,121,19,.65)"
    height="75vh"
    position="left center"
  >
    <v-container fill-height>
      <v-layout align-center>
        <v-flex text-xs-center light-text shadowed-text>
          <v-avatar :size="150" class="light-bg mb-2">
            <v-img
              :src="imageSource"
              alt="avatar"
            />
          </v-avatar>
          <h1 class="display-2 font-weight-bold text-uppercase mb-3">
            {{ name }}
          </h1>
          <div class="title font-weight-light text-uppercase mb-2">
            {{ function_ }}
          </div>
        </v-flex>
      </v-layout>
    </v-container>
  </v-img>
</template>

<script>
export default {
  data: () => ({
    name: 'SOFTLLAMA',
    function_: 'IT Consultancy',
    imageNumber: null,
    imageSource: null
  }),
  methods: {
    getRandomImage () {
      let validValues = ['02', '04', '09', '16']
      let i = Math.floor(Math.random() * validValues.length)
      return validValues[i]
    }
  },
  created () {
    this.imageNumber = this.getRandomImage()
    this.imageSource = require('@/assets/graphic-elements-' + this.imageNumber + '.png')
  }
}
</script>

<style scoped>
.light-bg {
    background-color: #f5f5f5;
    color: rgba(0,0,0,0.87);
}
.light-text {
    color: #f5f5f5;
}
</style>
