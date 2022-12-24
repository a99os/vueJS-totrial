<template>
  <div>
    <comment-form @addComment="createComment" />
    <comment-list v-bind:comments="comments" @remove="removeComment" />
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
      comments: [
        { id: 1, name: "Abbos", phone: 123455, content: "Lorem ipsum conten" },
        { id: 2, name: "Sobir", phone: 32435, content: "Lorem ipsum conten" },
        { id: 3, name: "Qodir", phone: 5425332, content: "Lorem ipsum conten" },
      ],
      name: "",
      phone: "",
      content: "",
    };
  },
  methods: {
    createComment(comment) {
      this.comments.push(comment);
    },
    removeComment(comment) {
      this.comments = this.comments.filter((c) => c.id != comment.id);
    },
  },
};
</script>
<style></style>
