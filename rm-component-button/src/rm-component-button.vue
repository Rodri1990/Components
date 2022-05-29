<script>
  import {defineComponent} from 'vue';

  export default /*#__PURE__*/ defineComponent({
    name: 'WButton', // vue name
    props: {
      color: {
        type: String,
        default: 'green',
      },
      size: {
        type: String,
      },
      label: {
        type: String,
      },
    },
    data() {
      return {
        color: this.color,
        size: this.size,
      };
    },
    computed: {
      buildButtonClass() {
        const size = this.size;
        return `button ${size}-btn`;
      },
    },
    methods: {},
  });
</script>

<template>
  <div>
    <button :class="buildButtonClass">Button</button>
  </div>
</template>

<style scoped>
  .button {
    background: v-bind(color);
    font-family: candara, arial, helvética;
    font-size: v-bind(size);
    color: white;
    width: 90px;
    height: 40px;
    border: 1px solid v-bind(color);
    border-radius: 6px;
    padding: 2px;
    margin: 2px;
  }

  /*Cuando hago hover con la propiedad filter aumento el brillo en 1.2  
    y con transition hago la animacion
  */
  .button:hover {
    transition: 0.2s linear 0.1s;
    filter: brightness(1.2);
  }
  .small-btn {
    width: 50px;
    height: 25px;
  }

  .medium-btn {
    width: 70px;
    height: 30px;
  }

  .large-btn {
    width: 90px;
    height: 40px;
  }

  .x-large-btn {
    width: 110px;
    height: 60px;
  }
  .xl-large-btn {
    width: 130px;
    height: 80px;
  }
</style>
