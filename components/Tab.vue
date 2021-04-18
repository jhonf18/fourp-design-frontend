<template>
<transition :name="tabs">
    <div v-show="isActive" style="background-color: #000">
      <slot></slot>
    </div>
</transition>
</template>

<script>
export default {
  name: 'Tab',
  props: {
    name: {required: true},
    selected: { default: false },
    low: { default: false }
  },data() {
    return {
      isActive: false
    };
  },
  computed: {
    href() {
      if(this.name.toLowerCase() == 'arquitectónico') {
        return '#' + 'arquitectonico';
      } else if( this.name.toLowerCase() == 'ilustración' ){
        return '#' + 'ilustracion'
      } else if(this.name.toLowerCase() === 'animación'){
        return '#' + 'animacion';
      }
      else {
        return '#' + this.name.toLowerCase().replace(/ /g, '-');
        }
    },
    tabs(){
      if(this.low) {
        return 'tabs-low'
      } else {
        return 'tabs'
      }
    }
  },
  mounted() {
    this.isActive = this.selected;
  }
}
</script>


<style lang="scss" scoped>
.col-md-3{
	margin: auto;
}

table{
  border: 1px solid black;
  text-align: center;
}

.title{
	background-color: blue;
	color: #fff;
	font-weight: bold;
	font-size: 18px;
}

.tabs-enter-active, .component-fade-leave-active {
  transition: opacity 1.1s ease;
}
.tabs-enter, .component-fade-leave-to
/* .component-fade-leave-active below version 2.1.8 */ {
  opacity: 0.7;
}

.tabs-low-enter-active, .component-fade-leave-active {
  transition: opacity .5s ease;
}
.tabs-low-enter, .component-fade-leave-to
/* .component-fade-leave-active below version 2.1.8 */ {
  opacity: 0.7;
}
</style>
