<template>
  <div>
    <comment-form @addComment="createComment" />
    <comment-list v-bind:comments="comments" />
  </div>
</template>
<script>
import CommentForm from "./components/CommentForm.vue";
import CommentList from "./components/CommentList";
export default {
  components: {
    CommentForm,
    CommentList,
  },
  data() {
    return {
      comments: [],
      name: "",
      phone: "",
      content: "",
    };
  },
  methods: {
    createComment(comment) {
      this.comments.push(comment);
    },
  },
};
</script>
<style></style>
