<template>
  <div>
    <comment-item
      class="w-75 mx-auto comment"
      v-for="comment in comments"
      :comment="comment"
      v-bind:key="comment.id"
    />
  </div>
</template>

<script>
import CommentItem from "./CommentItem";

export default {
  components: { CommentItem },
  props: {
    comments: {
      type: Array,
      required: true,
    },
  },
};
</script>
<style scoped>

</style>
