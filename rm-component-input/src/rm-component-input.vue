<script>
  import {defineComponent} from 'vue';

  export default /*#__PURE__*/ defineComponent({
    name: 'RmComponentInput', // name of component
    data() {
      return {
        label: this.label,
        type: this.type,
        placeholder: this.placeholder,
      };
    },
    props: {
      type: {
        type: String,
        default: 'text',
      },
      placeholder: {
        type: String,
      },
      label: {
        type: String,
      },
    },
    computed: {
      buildInputClass() {
        return `input ${this.type}`;
      },
    },
    methods: {},
  });
</script>

<template>
  <div class="root-input">
    <input
      :id="label"
      :placeholder="placeholder"
      :class="buildInputClass"
      :type="type"
      :name="label"
    />

    <!--<input
      id="text"
      placeholder="Nombre"
      class="input text"
      type="text"
      name="text"
    />
    -->
  </div>
</template>

<style scoped>
  * {
    font-family: candara, arial, helvética;
    margin: 4px 0 4px 0;
    color: white;
  }
  .root-input {
    display: flex;
    flex-direction: row;
  }

  label {
    padding: 4px;
    font-size: 16px;
  }

  input::placeholder {
    color: white;
  }

  input.text,
  input.email,
  input.password {
    padding: 15px;
    border: none;
    border-radius: 7px;
    background: #a9abb6;
    margin-bottom: 10px;
    box-sizing: border-box;
    outline-color: #898b95;
    color: white;
    font-size: 16px;
    width: 100%;
    text-align: left;
  }
</style>
