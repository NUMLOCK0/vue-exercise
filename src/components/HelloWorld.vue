<template>
  <div class="hello">
    <span>{{count}}</span>
    <span>{{msg1}}</span>
    <button @click="add">+</button>
    <button>-</button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg:String
  },
  data: function() {
    return {
      //msg:String
    };
  },
  computed: {
    count(){
      return  this.$store.state.count
    },
    msg1(){
      return this.msg + '233243'
    }
  },
  mounted() {
    //const {count} =
    console.log(this, '{{store}}')
  },
  methods:{
    add(){
      const {commit} = this.$store
      // const that = this
      commit('add')
      
    }
  }

};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
