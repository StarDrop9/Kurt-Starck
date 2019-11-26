<template>
  <div>
    <Welcome />
    <AboutMe />
    <OpenSource />
    <Services />
    <Certificates />
  </div>
</template>

<script>
import Welcome from '@/components/Welcome.vue'
import AboutMe from '@/components/AboutMe.vue'
import OpenSource from '@/components/OpenSource.vue'
import Services from '@/components/Services.vue'
import Certificates from '@/components/Certificates.vue'

export default {
  name: 'Content',
  components: {
    Welcome,
    AboutMe,
    OpenSource,
    Services,
    Certificates
  }
}
</script>
