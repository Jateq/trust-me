<script>
export default {
  data() {
    return {
      screenHeight: window.innerHeight + 'px', // Get the initial screen height and convert it to a string with 'px'
    };
  },
  mounted() {
    window.addEventListener('resize', this.updateScreenHeight);
  },
  beforeDestroy() {
    window.removeEventListener('resize', this.updateScreenHeight);
  },
  methods: {
    updateScreenHeight() {
      this.screenHeight = window.innerHeight + 'px';
    },
  },
};
</script>

<style scoped>
.container {
  --screen-height: {{ screenHeight }}; /* Define a CSS variable with the initial screen height */
}
</style>
