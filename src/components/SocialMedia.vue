<template>
  <div>
    <v-tooltip :bottom="bottom" :top="top" v-for="(item, i) in items" :key="i">
      <v-btn
        flat
        icon
        :small="small"
        :class="customClass"
        color="grey darken-1"
        :href="item.link"
        target="_blank"
        :key="i"
        slot="activator"
      >
        <v-icon :small="small" dark v-text="item.icon" />
      </v-btn>
      <span>{{ item.name }}</span>
    </v-tooltip>
  </div>
</template>

<script>
export default {
  name: 'SocialMedia',
  props: {
    bottom: Boolean,
    top: Boolean,
    customClass: String,
    small: String
  },
  data() {
    return {
      items: [
        {
          name: 'FCC',
          icon: 'mdi-fire',
          link: 'https://www.freecodecamp.org/StarDrop9'
        },
        {
          name: 'GitHub',
          icon: 'mdi-github-circle',
          link: 'https://www.github.com/stardrop9'
        },
        {
          name: 'LinkedIn',
          icon: 'mdi-linkedin',
          link: 'https://www.linkedin.com/in/kurt-starck-89390149'
        },
        {
          name: 'Twitter',
          icon: 'mdi-twitter',
          link: 'https://www.twitter.com/silversurfer691'
        },
        {
          name: 'Email',
          icon: 'mdi-email',
          link: 'mailto:kurtstarck@yahoo.com'
        }
      ]
    }
  }
}
</script>
