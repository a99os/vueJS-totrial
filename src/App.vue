<template>
  <div class="comment" v-for="comment in comments" v-bind:key="comment.id">
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
    };
  },
  methods: {
    increment() {
      this.count++;
    },
    decrement() {
      this.count--;
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
