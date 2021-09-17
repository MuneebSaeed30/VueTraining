<template>
  <div>
    <h1>Slot Component</h1>
    <!-- <slot> <h1> This is the default slot content </h1></slot> -->
    <!-- <slot name="namedSlot"> <h1> This is the default named slot content </h1> </slot> -->
    <slot name="scopedSlot" :trainer1="trainer1" :trainer2="trainer2"> {{ trainer1.firstName }} {{ trainer1.lastName }} </slot>
  </div>
</template>

<script>
export default {
  name: 'SlotComponent',
  data() {
      return {
          trainer1: {
              firstName: 'Muneeb',
              lastName: 'Saeed',
          },
          trainer2: {
              firstName: 'Abdullah',
              lastName: 'Khokar',
          },

      }
  }
}
</script>

