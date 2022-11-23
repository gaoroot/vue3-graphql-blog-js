<template>
  <div class="about">
    <AboutComponentVue msg="About componen VUE"/>
  </div>
</template>

<script>
import AboutComponentVue from '@/components/AboutComponent.vue';

export default {
  name: 'AboutView',
  components: {
    AboutComponentVue
  }
}
</script>