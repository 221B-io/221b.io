<template>
  <span class="textra">
    <span class="mainTextra" v-html="currentWord" :style="mainStyleComputed"></span>
  </span>
</template>

<script>
export default {
  name: 'Textra',
  props: {
    data: {
      type: Array,
      required: true
    },
    filter: {
      type: String,
      default: 'simple'
    },
    timer: {
      type: Number,
      default: 1
    },
    infinite: {
      type: Boolean,
      default: false
    }
  },
  data() {
    return {
      defaultStyle: 'transition: ' + this.timer + 's;',
      currentWord: this.data[0],
      liStl: 'opacity:0;',
      dataCounter: 0,
      displayState: 0,
      filters: {
        simple: ['opacity:0', 'opacity:1']
      }
    };
  },
  computed: {
    mainStyleComputed() {
      return this.defaultStyle + this.liStl;
    }
  },
  created() {
    var theInterval = setInterval(() => {
      if (this.displayState === 0) {
        // fade in
        this.liStl = this.filters[this.filter][1];
        this.displayState = 1;
        this.dataCounter++;
        if (this.dataCounter === this.data.length) {
          this.dataCounter = 0;
        }
        this.currentWord = this.data[this.dataCounter];
      } else if (this.displayState === 1) {
        // stay faded in
        this.liStl = this.filters[this.filter][1];
        this.displayState = 2;
      } else if (this.displayState === 2) {
        // stay faded in
        this.liStl = this.filters[this.filter][1];
        this.displayState = 3;
      } else {
        // fade out
        this.liStl = this.filters[this.filter][0];
        this.displayState = 0;
      }
      if (this.dataCounter === this.data.length) {
        clearInterval(theInterval);
      }
    }, +this.timer * 1000);
  }
};
</script>

<style scoped>
.textra {
  height: auto;
  width: auto;
  display: inline;
}
</style>



