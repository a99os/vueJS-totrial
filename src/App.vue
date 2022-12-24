<template>
  <div>
    <p>
      Count: <strong>{{ count }}</strong>
    </p>
  </div>
  <button class="btn btn-success" @:click="increment">Increment</button>
  <button class="btn btn-primary" v-on:click="decrement">Decrement</button>
</template>
<script>
export default {
  data() {
    return {
      count: 0,
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
<style></style>
