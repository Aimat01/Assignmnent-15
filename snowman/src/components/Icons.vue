  <template>
    <i :class="iconClasses"></i>
  </template>
  
  <script>
  export default {
    props: {
      name: {
        type: String,
        required: true
      }
    },
    computed: {
      iconClasses() {
        return `icon-${this.name}`;
      }
    }
  }
  </script>
  
  <style scoped>
  
  .icon-home {
    display: inline-block;
    width: 24px;
    height: 24px;
    background: url('./assets/home.svg') no-repeat center center;
  }
  
  .icon-settings {
    display: inline-block;
    width: 24px;
    height: 24px;
    background: url('./assets/settings.svg') no-repeat center center;
  }
  </style>
  
  