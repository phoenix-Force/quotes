<template>
  <div class="row">
   <form >
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 from-group">
        <label for="adding-quote">Quote</label>
        <textarea name="" id="" rows="3" class ="form-control" v-model="quote"></textarea>
    </div>
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 from-group">
        <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
      </div>

   </form>
  </div>

</template>
<script>
export default {
  data:()=>{
    return{
      quote:''
    }
  },
  methods:{
    createNew(){
      if(this.quote ===''){
        alert("write something")
      }else{
        this.$emit("quoteAdded",this.quote);
      this.quote=""
      }

    }
  }

}
</script>
<style  scoped>

</style>
