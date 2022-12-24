<template>
  <div>
    <p>
      {{ comment.name }}-

      <b>{{ comment.phone }}</b>
    </p>
    <p><b>Content:</b>{{ comment.content }}</p>
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
