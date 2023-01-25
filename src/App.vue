<template>
  <div>
    <header>
      <router-link to="/login">로그인</router-link> |
      <router-link to="/signup">회원가입</router-link>
    </header>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'VueTilApp',

  data() {
    return {};
  },

  mounted() {},

  methods: {},
};
</script>

<style lang="scss" scoped></style>
