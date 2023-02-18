<template>
  <div>
    <AppHeader></AppHeader>
    <router-view></router-view>
  </div>
</template>

<script>
import AppHeader from '@/components/common/AppHeader.vue';

export default {
  name: 'VueTilApp',

  components: {
    AppHeader,
  },

  data() {
    return {};
  },

  created() {
    console.log(process.env);
  },

  methods: {},
};
</script>

<style lang="scss" scoped></style>
