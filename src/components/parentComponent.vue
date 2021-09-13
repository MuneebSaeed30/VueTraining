<template>
  <div>
    <ChildComponent message="Static content" @messageFromChild="messageReceived" />
        <!-- <ChildComponent :message="message"/> -->
  </div>
</template>

<script>
import ChildComponent from './childComponent'

export default {
  name: 'ParentComponent',
  data() {
    return {
        message: 'Dynamic content'
      }
  },
  methods: {
      messageReceived(arg1, arg2) {
          console.log('message from child', arg1, arg2);
      }
  },
  components: {
      ChildComponent,
  }
}
</script>

