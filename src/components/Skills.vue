<template>
  <section-layout title="skills">
    <v-layout row wrap>
      <v-flex xs12 md6
        v-for="item in barDetails"
        :key="item.name">
        <div class="mb-4 mx-5">
          <v-layout row wrap>
            <i style="font-size: x-large;" :class="item.icon" :style="'color:'+item.color+';'"/>
            <div class="subheading blue-grey--text text--darken-3 ml-2"> {{ item.name }} </div>
          </v-layout>
          <v-progress-linear
            class="mb-4 mt-1"
            :color="item.color"
            :value="item.value"
          />
        </div>
      </v-flex>
    </v-layout>
  </section-layout>
</template>

<script>
import COLORS from '@/constants/colors.js'
import SectionLayout from '@/components/SectionLayout'

export default {
  components: {
    SectionLayout
  },
  data: () => ({
    items: [
      // Generated using a small python script by hitting 'https://konpa.github.io/devicon/devicon.git/devicon.json'
      { name: 'amazonwebservices', icon: 'devicon-amazonwebservices-original', value: 66 },
      { name: 'css3', icon: 'devicon-css3-plain', value: 66 },
      { name: 'django', icon: 'devicon-django-plain', value: 80 },
      { name: 'docker', icon: 'devicon-docker-plain', value: 50 },
      { name: 'git', icon: 'devicon-git-plain', value: 90 },
      { name: 'html5', icon: 'devicon-html5-plain', value: 66 },
      { name: 'java', icon: 'devicon-java-plain', value: 45 },
      { name: 'javascript', icon: 'devicon-javascript-plain', value: 75 },
      { name: 'jquery', icon: 'devicon-jquery-plain', value: 75 },
      { name: 'linux', icon: 'devicon-linux-plain', value: 85 },
      { name: 'nginx', icon: 'devicon-nginx-original', value: 65 },
      { name: 'photoshop', icon: 'devicon-photoshop-plain', value: 33 },
      { name: 'postgresql', icon: 'devicon-postgresql-plain', value: 90 },
      { name: 'python', icon: 'devicon-python-plain', value: 90 },
      { name: 'react', icon: 'devicon-react-original', value: 33 },
      { name: 'ssh', icon: 'devicon-ssh-plain', value: 90 },
      { name: 'vim', icon: 'devicon-vim-plain', value: 80 },
      { name: 'vuejs', icon: 'devicon-vuejs-plain', value: 80 }
    ],
    used_colors: []
  }),
  methods: {
    getRandomColor () {
      let i = Math.floor(Math.random() * COLORS.length)
      if (this.used_colors.includes(i)) {
        return this.getRandomColor()
      } else {
        this.used_colors.push(i)
        return COLORS[i]
      }
    },
    compare (a, b) {
      if (a.value < b.value) {
        return 1
      } else if (a.value > b.value) {
        return -1
      } else {
        return 0
      }
    }
  },
  computed: {
    barDetails () {
      const result = []
      for (let index = 0; index < this.items.length; index++) {
        const element = this.items[index]
        element['color'] = this.getRandomColor()
        result.push(element)
      }
      return result.sort(this.compare)
    }
  }
}
</script>
