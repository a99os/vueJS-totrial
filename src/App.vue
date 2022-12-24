<template>
  <div class="w-75 mx-auto">
    <h3>Add comment</h3>
    <form>
      <input
        @input="name = $event.target.value"
        :value="name"
        type="text"
        placeholder="Enter your name"
        class="form-control"
      />
      <input
        @input="phone = $event.target.value"
        :value="phone"
        type="text"
        placeholder="Enter your phone"
        class="form-control my-3"
      />
      <input
        @input="content = $event.target.value"
        :value="content"
        type="text"
        placeholder="Enter your content"
        class="form-control"
      />
      <div class="d-flex flex-row-reverse">
        <button @click="createComment" class="btn btn-primary mt-3">
          Add Comment
        </button>
      </div>
    </form>
  </div>
  <div
    class="w-75 mx-auto comment"
    v-for="comment in comments"
    v-bind:key="comment.id"
  >
    <div><b>Name:</b>{{ comment.name }}</div>
    <div><b>Phone:</b>{{ comment.phone }}</div>
    <div><b>Content:</b>{{ comment.content }}</div>
  </div>
</template>
<script>
export default {
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
    createComment(e) {
      e.preventDefault();
      this.comments.push({
        id: this.comments.length + 1,
        name: this.name,
        phone: this.Phone,
        content: this.content,
      });
      this.name = "";
      this.phone = "";
      this.content = "";
    },
  },
};
</script>
<style>
.comment {
  border: 5px solid #ccc;
  padding: 10px;
  margin: 10px;
}
</style>
