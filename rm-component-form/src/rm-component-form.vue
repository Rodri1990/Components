<script>
  import {defineComponent} from 'vue';

  export default defineComponent({
    name: 'RmComponentForm', // name of component
    props: {
      title: {
        type: String,
      },
    },
    data() {
      return {
        title: this.title,
      };
    },
  });
</script>

<template>
  <form action="" class="form-fields">
    <fieldset class="">
      <legend>{{ title }}</legend>
      <slot></slot>
    </fieldset>
  </form>
</template>

<style scoped>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  fieldset {
    border: none;
  }

  legend {
    color: white;
    display: flex;
    text-align: center;
    padding: 14px;
  }
  h3 {
    justify-content: center;
    color: white;
  }

  .form-fields {
    display: flex;
    flex-direction: column;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-49%, -49%);
    width: 100%;
    height: 100%;
    max-width: 450px;
    max-height: 450px;
    padding: 0px 10px 10px 10px;
    border-radius: 10px;
    background-color: #444763;
    box-shadow: 0 0 15px 1px rgba(0, 0, 0, 0.3);
  }
  .rm-component-form {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-49%, -49%);
    width: 100%;
    height: 100%;
    max-width: 450px;
    max-height: 450px;
    padding: 0px 10px 10px 10px;
    border-radius: 10px;
    background-color: #444763;
  }
</style>
