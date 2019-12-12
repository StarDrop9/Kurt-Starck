<template>
  <section id="about" class="hide-overflow">
    <v-layout>
      <v-flex xs12 v-show="$vuetify.breakpoint.smAndDown">
        <v-img height="100%" width="100%" :src="require('@/assets/kps2.jpg')" />
      </v-flex>
    </v-layout>
    <v-layout light-blue lighten-2 white--text>
      <v-flex md6>
        <v-img :src="require('@/assets/about-me.jpg')" height="100%" />
      </v-flex>
      <v-flex xs12 md6 pa-5>
        <Heading v-html="$t('about_me.TITLE')" />
        <ContentText v-html="$t('about_me.PARAGRAPH_1')" />
        <ContentText v-html="$t('about_me.PARAGRAPH_2')" />
        <ContentText v-html="$t('about_me.PARAGRAPH_3')" />
        <ContentText>
          <v-layout
            v-for="(skill, i) in skills"
            :key="i"
            style="color: #69A1BB;"
            wrap
            white--text
            d-inline
          >
            <v-chip color="white">
              <img
                :src="require(`@/assets/logos/${skill.imageURL}`)"
                class="logo"
              />
              {{ skill.name }}
            </v-chip>
          </v-layout>
        </ContentText>
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
export default {
  name: 'AboutMe',
  data: () => ({
    skills: [
      {
        name: 'ES6',
        imageURL: 'js.png'
      },
      {
        name: 'NodeJS',
        imageURL: 'nodejs.png'
      },
      {
        name: 'VueJS',
        imageURL: 'vue.png'
      },
      {
        name: 'HTML',
        imageURL: 'html.png'
      },
      {
        name: 'CSS',
        imageURL: 'css.png'
      },
      {
        name: 'MongoDB',
        imageURL: 'mongodb.png'
      },
      {
        name: 'MySQL',
        imageURL: 'mysql.png'
      },
      {
        name: 'IBM Domino Stack',
        imageURL: 'IBMNotes.png'
      },
      {
        name: 'D3.js & Data Visualization',
        imageURL: 'd3js.png'
      },
      {
        name: 'PHP',
        imageURL: 'php.png'
      },
      {
        name: 'Angular',
        imageURL: 'ng.png'
      },
      {
        name: 'Ubuntu & Linux',
        imageURL: 'ubuntu.png'
      },
      {
        name: 'MEAN Stack',
        imageURL: 'meanstack.png'
      },
      {
        name: 'WAMP Stack',
        imageURL: 'wamp.png'
      },
      {
        name: 'Express',
        imageURL: 'express.png'
      },
      {
        name: 'React',
        imageURL: 'react.png'
      },
      {
        name: 'Vanilla.Js',
        imageURL: 'vanillajs.png'
      },
      {
        name: 'Jquery',
        imageURL: 'jquery.png'
      },
      {
        name: 'Docker and Circle.io',
        imageURL: 'docker.png'
      }
    ]
  })
}
</script>

<style scoped>
.logo {
  height: 18px;
  margin-right: 7px;
}
</style>
