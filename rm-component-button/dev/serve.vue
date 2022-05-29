<script>
import { defineComponent } from 'vue';
import RmComponentButton from '@/rm-component-button.vue';

export default defineComponent({
  name: 'ServeDev',
  components: {
    RmComponentButton
  }
});
</script>

<template>
  <div id="app">
    <rm-component-button />
  </div>
</template>
