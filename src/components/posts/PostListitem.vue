<template>
  <ul>
    <li>
      <div class="post-title">
        {{ postItem.title }}
      </div>
      <div class="post-contents">
        {{ postItem.contents }}
      </div>
      <div class="post-time">
        {{ postItem.createdAt }}
      </div>
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: {
    postItem: {
      type: Object,
      required: true,
    },
  },

  mounted() {},

  methods: {},
};
</script>

<style lang="scss" scoped></style>
