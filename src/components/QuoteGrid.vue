<template>
  <div class ="row">
    <quote-c :key ="index" v-for = "(q,index) in quotes" @click.native="dlt(index)">{{q}}</quote-c>
  </div>

</template>
<script>
import quote from "./Quote.vue"
export default {
  props:['quotes'],
  components:{
    quoteC:quote
  },
  methods:{
    dlt(index){
      this.$emit("deleted",index)
    }
  }


}
</script>
<style scoped>

</style>
