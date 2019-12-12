/* eslint-disable */
<template>
  <section id="certificates" class="hide-overflow">
   <v-layout light-blue lighten-2 white--text wrap>
     <v-flex xs12 md6 > 
      <v-layout light-blue lighten-2 white--text>
         <v-flex xs12 pa-5>
            <Heading v-html="$t('certificates.TITLE')" />
            <ContentText v-html="$t('certificates.PARAGRAPH_1')" />
            <ContentText v-html="$t('certificates.PARAGRAPH_2')" />
            <ContentText v-html="$t('certificates.PARAGRAPH_3')" />
         </v-flex>
        </v-layout>
        <v-container class="mx-0">
          <v-layout row wrap light-blue lighten-2  >
           <v-flex xs12 sm6 v-for="(cert, i) in certs" :key="i">
            <v-card flat class="text-xs-center ma-2">
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
     <v-flex> 
       <v-img :src="require('@/assets/certificate333resize.jpg')" height="100%" width="100%"/>
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
        name: 'JS Algos & Data Structs',
        imageURL: 'jsalgosdata.png'
      },
      {
        name: 'Front End Libraries',
        imageURL: 'FrontEndLib.png'
      },
      {
        name: 'Responsive Web Design',
        imageURL: 'ResponsiveWebDesign.png'
      },
      {
        name: 'Web App Pentesting',
        imageURL: 'WebAppPentesting.png'
      },
      {
        name: 'Metasploit',
        imageURL: 'Metasploit.png'
      },
      {
        name: 'Nessus',
        imageURL: 'Nessus.png'
      },
      {
        name: 'Intro to Python',
        imageURL: 'IntroToPython.png'
      },
      {
        name: 'Advanced Pentesting',
        imageURL: 'AdvancedPentesting.png'
      },
       {
        name: 'Crypto Fundamentals',
        imageURL: 'CryptoFundamentals.png'
      },
      {
        name: 'CompTia CASP',
        imageURL: 'CompTiaCASP.png'
      },
      {
        name: 'Certified Lotus Notes Professional',
        imageURL: 'clpb.png'
      }
     ]
  })
}
</script>

<style lang="scss" scoped>

.logo {
  width: 100px;
  height: 80px;
  margin-right: 0px;
}
.card {
    margin-bottom: 3px;
    border-radius: 10%;
   }

</style>

