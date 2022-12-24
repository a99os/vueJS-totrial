<template>
  <div class="comment">
    <div>
      <p>
        {{ comment.name }}-<b>{{ comment.phone }}</b>
      </p>
      <p><b>Content:</b>{{ comment.content }}</p>
    </div>
    <div>
      <my-button class="btn btn-danger">Delete</my-button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    comment: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style scoped>
.comment {
  border: 5px solid #ccc;
  padding: 10px;
  margin: 10px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>
