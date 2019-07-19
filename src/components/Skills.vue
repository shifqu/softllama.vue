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
import SectionLayout from '../components/SectionLayout'

export default {
  components: {
    SectionLayout
  },
  data: () => ({
    items: [
      // Generated using a small python script by hitting 'https://konpa.github.io/devicon/devicon.git/devicon.json'
      { name: 'amazonwebservices', icon: 'devicon-amazonwebservices-original', value: 66 },
      // { name: 'android', icon: 'devicon-android-plain', value: 33 },
      // { name: 'angularjs', icon: 'devicon-angularjs-plain', value: 33 },
      // { name: 'apache', icon: 'devicon-apache-plain', value: 50 },
      // { name: 'appcelerator', icon: 'devicon-appcelerator-original', value: 33 },
      // { name: 'apple', icon: 'devicon-apple-original', value: 80 },
      // { name: 'atom', icon: 'devicon-atom-original', value: 33 },
      // { name: 'babel', icon: 'devicon-babel-plain', value: 33 },
      // { name: 'backbonejs', icon: 'devicon-backbonejs-plain', value: 33 },
      // { name: 'bitbucket', icon: 'devicon-bitbucket-plain', value: 33 },
      // { name: 'bootstrap', icon: 'devicon-bootstrap-plain', value: 33 },
      // { name: 'bower', icon: 'devicon-bower-plain', value: 33 },
      // { name: 'c', icon: 'devicon-c-plain', value: 33 },
      // { name: 'chrome', icon: 'devicon-chrome-plain', value: 33 },
      // { name: 'codeigniter', icon: 'devicon-codeigniter-plain', value: 33 },
      // { name: 'coffeescript', icon: 'devicon-coffeescript-original', value: 33 },
      // { name: 'confluence', icon: 'devicon-confluence-plain', value: 33 },
      // { name: 'cplusplus', icon: 'devicon-cplusplus-plain', value: 33 },
      // { name: 'csharp', icon: 'devicon-csharp-plain', value: 33 },
      { name: 'css3', icon: 'devicon-css3-plain', value: 66 },
      // { name: 'cucumber', icon: 'devicon-cucumber-plain', value: 33 },
      // { name: 'd3js', icon: 'devicon-d3js-plain', value: 33 },
      // { name: 'debian', icon: 'devicon-debian-plain', value: 75 },
      // { name: 'devicon', icon: 'devicon-devicon-plain', value: 33 },
      { name: 'django', icon: 'devicon-django-plain', value: 80 },
      { name: 'docker', icon: 'devicon-docker-plain', value: 50 },
      // { name: 'doctrine', icon: 'devicon-doctrine-plain', value: 33 },
      // { name: 'dot-net', icon: 'devicon-dot-net-plain', value: 33 },
      // { name: 'drupal', icon: 'devicon-drupal-plain', value: 33 },
      // { name: 'erlang', icon: 'devicon-erlang-plain', value: 33 },
      // { name: 'express', icon: 'devicon-express-original', value: 33 },
      // { name: 'facebook', icon: 'devicon-facebook-plain', value: 33 },
      // { name: 'firefox', icon: 'devicon-firefox-plain', value: 33 },
      // { name: 'foundation', icon: 'devicon-foundation-plain', value: 33 },
      // { name: 'gatling', icon: 'devicon-gatling-plain', value: 33 },
      // { name: 'gimp', icon: 'devicon-gimp-plain', value: 33 },
      { name: 'git', icon: 'devicon-git-plain', value: 90 },
      // { name: 'github', icon: 'devicon-github-plain', value: 33 },
      // { name: 'gitlab', icon: 'devicon-gitlab-plain', value: 33 },
      // { name: 'go', icon: 'devicon-go-plain', value: 33 },
      // { name: 'google', icon: 'devicon-google-plain', value: 33 },
      // { name: 'gradle', icon: 'devicon-gradle-plain', value: 33 },
      // { name: 'grunt', icon: 'devicon-grunt-plain', value: 33 },
      // { name: 'gulp', icon: 'devicon-gulp-plain', value: 33 },
      // { name: 'heroku', icon: 'devicon-heroku-original', value: 33 },
      { name: 'html5', icon: 'devicon-html5-plain', value: 66 },
      // { name: 'ie10', icon: 'devicon-ie10-original', value: 33 },
      // { name: 'illustrator', icon: 'devicon-illustrator-plain', value: 33 },
      // { name: 'inkscape', icon: 'devicon-inkscape-plain', value: 33 },
      // { name: 'intellij', icon: 'devicon-intellij-plain', value: 33 },
      { name: 'java', icon: 'devicon-java-plain', value: 45 },
      // { name: 'jasmine', icon: 'devicon-jasmine-plain', value: 33 },
      { name: 'javascript', icon: 'devicon-javascript-plain', value: 75 },
      // { name: 'jeet', icon: 'devicon-jeet-plain', value: 33 },
      // { name: 'jetbrains', icon: 'devicon-jetbrains-plain', value: 33 },
      { name: 'jquery', icon: 'devicon-jquery-plain', value: 75 },
      // { name: 'krakenjs', icon: 'devicon-krakenjs-plain', value: 33 },
      // { name: 'laravel', icon: 'devicon-laravel-plain', value: 33 },
      // { name: 'less', icon: 'devicon-less-plain-wordmark', value: 33 },
      { name: 'linux', icon: 'devicon-linux-plain', value: 85 },
      // { name: 'meteor', icon: 'devicon-meteor-plain', value: 33 },
      // { name: 'mocha', icon: 'devicon-mocha-plain', value: 33 },
      // { name: 'mongodb', icon: 'devicon-mongodb-plain', value: 33 },
      // { name: 'moodle', icon: 'devicon-moodle-plain', value: 33 },
      // { name: 'mysql', icon: 'devicon-mysql-plain', value: 33 },
      { name: 'nginx', icon: 'devicon-nginx-original', value: 65 },
      // { name: 'nodejs', icon: 'devicon-nodejs-plain', value: 33 },
      // { name: 'nodewebkit', icon: 'devicon-nodewebkit-plain', value: 33 },
      // { name: 'oracle', icon: 'devicon-oracle-original', value: 33 },
      { name: 'photoshop', icon: 'devicon-photoshop-plain', value: 33 },
      // { name: 'php', icon: 'devicon-php-plain', value: 33 },
      // { name: 'phpstorm', icon: 'devicon-phpstorm-plain', value: 33 },
      // { name: 'protractor', icon: 'devicon-protractor-plain', value: 33 },
      { name: 'postgresql', icon: 'devicon-postgresql-plain', value: 90 },
      { name: 'python', icon: 'devicon-python-plain', value: 90 },
      // { name: 'pycharm', icon: 'devicon-pycharm-plain', value: 33 },
      // { name: 'rails', icon: 'devicon-rails-plain', value: 33 },
      { name: 'react', icon: 'devicon-react-original', value: 33 },
      // { name: 'redhat', icon: 'devicon-redhat-plain', value: 33 },
      // { name: 'redis', icon: 'devicon-redis-plain', value: 33 },
      // { name: 'ruby', icon: 'devicon-ruby-plain', value: 33 },
      // { name: 'rubymine', icon: 'devicon-rubymine-plain', value: 33 },
      // { name: 'safari', icon: 'devicon-safari-plain', value: 33 },
      // { name: 'sass', icon: 'devicon-sass-original', value: 33 },
      // { name: 'sequelize', icon: 'devicon-sequelize-plain', value: 33 },
      // { name: 'slack', icon: 'devicon-slack-plain', value: 33 },
      // { name: 'sourcetree', icon: 'devicon-sourcetree-plain', value: 33 },
      { name: 'ssh', icon: 'devicon-ssh-plain', value: 90 },
      // { name: 'swift', icon: 'devicon-swift-plain', value: 33 },
      // { name: 'symfony', icon: 'devicon-symfony-original', value: 33 },
      // { name: 'tomcat', icon: 'devicon-tomcat-line', value: 33 },
      // { name: 'travis', icon: 'devicon-travis-plain', value: 33 },
      // { name: 'trello', icon: 'devicon-trello-plain', value: 33 },
      // { name: 'twitter', icon: 'devicon-twitter-plain', value: 33 },
      // { name: 'typescript', icon: 'devicon-typescript-plain', value: 33 },
      // { name: 'ubuntu', icon: 'devicon-ubuntu-plain', value: 33 },
      { name: 'vim', icon: 'devicon-vim-plain', value: 80 },
      // { name: 'visualstudio', icon: 'devicon-visualstudio-plain', value: 33 },
      { name: 'vuejs', icon: 'devicon-vuejs-plain', value: 80 }
      // { name: 'webpack', icon: 'devicon-webpack-plain', value: 33 },
      // { name: 'webstorm', icon: 'devicon-webstorm-plain', value: 33 },
      // { name: 'windows8', icon: 'devicon-windows8-original', value: 33 },
      // { name: 'wordpress', icon: 'devicon-wordpress-plain', value: 33 },
      // { name: 'yii', icon: 'devicon-yii-plain', value: 33 },
      // { name: 'zend', icon: 'devicon-zend-plain', value: 33 }
    ],
    colors: [
      // Generated using a small python script by hitting 'https://vuetifyjs.com/en/framework/colors'
      // and excluding any `lighten` variants
      '#F44336',
      '#E53935',
      '#D32F2F',
      '#C62828',
      '#B71C1C',
      '#FF8A80',
      '#FF5252',
      '#FF1744',
      '#D50000',
      '#E91E63',
      '#D81B60',
      '#C2185B',
      '#AD1457',
      '#880E4F',
      '#FF80AB',
      '#FF4081',
      '#F50057',
      '#C51162',
      '#9C27B0',
      '#8E24AA',
      '#7B1FA2',
      '#6A1B9A',
      '#4A148C',
      '#EA80FC',
      '#E040FB',
      '#D500F9',
      '#AA00FF',
      '#673AB7',
      '#5E35B1',
      '#512DA8',
      '#4527A0',
      '#311B92',
      '#B388FF',
      '#7C4DFF',
      '#651FFF',
      '#6200EA',
      '#3F51B5',
      '#3949AB',
      '#303F9F',
      '#283593',
      '#1A237E',
      '#8C9EFF',
      '#536DFE',
      '#3D5AFE',
      '#304FFE',
      '#2196F3',
      '#1E88E5',
      '#1976D2',
      '#1565C0',
      '#0D47A1',
      '#82B1FF',
      '#448AFF',
      '#2979FF',
      '#2962FF',
      '#03A9F4',
      '#039BE5',
      '#0288D1',
      '#0277BD',
      '#01579B',
      '#80D8FF',
      '#40C4FF',
      '#00B0FF',
      '#0091EA',
      '#00BCD4',
      '#00ACC1',
      '#0097A7',
      '#00838F',
      '#006064',
      '#84FFFF',
      '#18FFFF',
      '#00E5FF',
      '#00B8D4',
      '#009688',
      '#00897B',
      '#00796B',
      '#00695C',
      '#004D40',
      '#A7FFEB',
      '#64FFDA',
      '#1DE9B6',
      '#00BFA5',
      '#4CAF50',
      '#43A047',
      '#388E3C',
      '#2E7D32',
      '#1B5E20',
      '#B9F6CA',
      '#69F0AE',
      '#00E676',
      '#00C853',
      '#8BC34A',
      '#7CB342',
      '#689F38',
      '#558B2F',
      '#33691E',
      '#CCFF90',
      '#B2FF59',
      '#76FF03',
      '#64DD17',
      '#CDDC39',
      '#C0CA33',
      '#AFB42B',
      '#9E9D24',
      '#827717',
      '#F4FF81',
      '#EEFF41',
      '#C6FF00',
      '#AEEA00',
      '#FFEB3B',
      '#FDD835',
      '#FBC02D',
      '#F9A825',
      '#F57F17',
      '#FFFF8D',
      '#FFFF00',
      '#FFEA00',
      '#FFD600',
      '#FFC107',
      '#FFB300',
      '#FFA000',
      '#FF8F00',
      '#FF6F00',
      '#FFE57F',
      '#FFD740',
      '#FFC400',
      '#FFAB00',
      '#FF9800',
      '#FB8C00',
      '#F57C00',
      '#EF6C00',
      '#E65100',
      '#FFD180',
      '#FFAB40',
      '#FF9100',
      '#FF6D00',
      '#FF5722',
      '#F4511E',
      '#E64A19',
      '#D84315',
      '#BF360C',
      '#FF9E80',
      '#FF6E40',
      '#FF3D00',
      '#DD2C00',
      '#795548',
      '#6D4C41',
      '#5D4037',
      '#4E342E',
      '#3E2723',
      '#607D8B',
      '#546E7A',
      '#455A64',
      '#37474F',
      '#263238',
      '#9E9E9E',
      '#757575',
      '#616161',
      '#424242',
      '#212121',
      '#000000'
    ],
    used_colors: []
  }),
  methods: {
    getRandomColor () {
      let i = Math.floor(Math.random() * this.colors.length)
      if (this.used_colors.includes(i)) {
        // If
        return this.getRandomColor()
      } else {
        this.used_colors.push(i)
        return this.colors[i]
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
