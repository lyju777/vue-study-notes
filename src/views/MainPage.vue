<template>
  <div>
    <div class="main list-container contents">
      <h1 class="page-header">Today I Learned</h1>

      <LoadingSpinner v-if="isLoading"></LoadingSpinner>

      <ul v-else>
        <PostListitem
          v-for="postItem in postItems"
          :key="postItem._id"
          :postItem="postItem"
        ></PostListitem>
      </ul>
    </div>
  </div>
</template>

<script>
import PostListitem from '@/components/posts/PostListitem.vue';
import LoadingSpinner from 'LoadingSpinner';
import { fetchPosts } from '@/api/index';
export default {
  components: {
    PostListitem,
    LoadingSpinner,
  },
  data() {
    return {
      postItems: [],
      isLoading: false,
    };
  },
  methods: {
    async fetchData() {
      this.isLoading = true;
      const { data } = await fetchPosts();
      this.isLoading = false;
      this.postItems = data.posts;
    },
  },
  created() {
    this.fetchData();
  },
};
</script>

<style></style>
