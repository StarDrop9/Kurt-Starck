/* eslint-disable */
<template>
  <section id="certificates" class="hide-overflow">
    <v-layout>
      <v-flex xs12 md6 v-show="$vuetify.breakpoint.smAndDown">
        <v-img
          :src="require('@/assets/certificate.jpg')"
          height="100%"
          width="100%"
        />
      </v-flex>
    </v-layout>
    <v-layout light-blue lighten-2 white--text>
      <v-flex xs12 md6 pa-5>
        <Heading v-html="$t('certificates.TITLE')" />
        <ContentText v-html="$t('certificates.PARAGRAPH_1')" />
        <ContentText v-html="$t('certificates.PARAGRAPH_2')" />
        <ContentText v-html="$t('certificates.PARAGRAPH_3')" />
     </v-layout>
      <v-container class="my-3">
        <v-layout row wrap>
        <v-flex xs12 sm6 v-for="(cert, i) in certs" :key="i">
          <v-card flat class="text-xs-center ma-3">
          <v-responsive class="pt-1">
              <img
                :src="require(`@/assets/${cert.imageURL}`)"
                class="logo"
              />
          </v-responsive>
            <v-card-text>
              <div class="subheading">{{ cert.name }}</div>
            </v-card-text>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
      </v-flex>
      <v-flex md6>
        <v-img :src="require('@/assets/certificate33.jpg')" height="100%" />
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
export default {
  name: 'Certificates',
  data: () => ({
    certs: [
      {
        name: 'Comptia Sec+',
        imageURL: 'ComptiaCertified.png'
      },
      {
        name: 'JS Algorithms and Data Structures',
        imageURL: 'jsalgosdata.png'
      }
    /*  {
        name: 'VueJS',
        imageURL: 'vue.png'
      },*/
    ]
  })
}
</script>

<style scoped>
.logo {
  width: 170px;
  height: 160px;
  margin-right: 0px;
}
.card {
    margin-bottom: 10px;
    border-radius: 10%;
}
</style>
