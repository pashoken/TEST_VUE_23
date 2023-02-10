<template>
<draggable v-model="newArr" group="people" @start="drag=true" @end="drag=false">
   <div v-for="(element,index) in newArr" :key="index">{{element}}</div>
</draggable>
</template>

<script>
import draggable from 'vuedraggable'
export default {
  componets:{
    draggable,
  },
  data() {
    return {
      arr: 'слово',
      newArr: [],
      drag: false,
    };
  },

  mounted() {
    this.newArr = this.arr.split('').sort((qw) => Math.random() - 0.5);
    console.log(this.newArr);
  },
  methods: {
    asd(){
      console.log("asdsadasdsad");
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
.qwe 
  display: flex
  width: 50vw
  height: 300px
  align-self: center
  justify-content: space-between
  align-items: center
  

</style>