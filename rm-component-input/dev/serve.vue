<script>
import { defineComponent } from 'vue';
import RmComponentInput from '@/rm-component-input.vue';

export default defineComponent({
  name: 'ServeDev',
  components: {
    RmComponentInput
  }
});
</script>

<template>
  <div id="app">
    <rm-component-input />
  </div>
</template>
