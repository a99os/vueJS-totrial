<template>
  <div>
    <div class="w-75 mx-auto">
      <h3>Add comment</h3>
      <form @submit.prevent>
        <my-input
          v-model="comment.name"
          type="text"
          placeholder="Enter your name"
          class="form-control"
        />
        <my-input
          v-model="comment.phone"
          type="text"
          placeholder="Enter your phone"
          class="form-control my-3"
        />
        <my-input
          v-model="comment.content"
          type="text"
          placeholder="Enter your content"
          class="form-control"
        />
        <div class="d-flex flex-row-reverse">
          <my-button @click="createComment" class="btn btn-primary mt-3">
            Add Comment
          </my-button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      comment: {
        name: "",
        phone: "",
        content: "",
      },
    };
  },

  methods: {
    createComment() {
      this.comment.id = Date.now();
      this.$emit("addComment", this.comment);
      this.comment = {
        name: "",
        phone: "",
        content: "",
      };
    },
  },
};
</script>
<style></style>
