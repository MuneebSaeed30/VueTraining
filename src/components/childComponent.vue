<template>
  <div>
    <h1>{{ message }}</h1>
    <button @click="sendMessageToParent"> Invoke Parent Function </button>
  </div>
</template>

<script>
export default {
  name: 'ChildComponent',
  props: {
    message: String
  },
  methods: {
      sendMessageToParent() {
          this.$emit('messageFromChild', 1, true);
      }
  }
}
</script>

