<script>
import { defineComponent } from 'vue';
import RmComponentForm from '@/rm-component-form.vue';

export default defineComponent({
  name: 'ServeDev',
  components: {
    RmComponentForm
  }
});
</script>

<template>
  <div id="app">
    <rm-component-form />
  </div>
</template>
