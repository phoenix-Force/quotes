<template>
<div class="cointainer">
  <p-head :qCount="quotes.length" :Max="maxQuote"></p-head>
  <n-quote @quoteAdded ="added"></n-quote>
  <g-quotes :quotes="quotes" @deleted="deletethis" ></g-quotes>
</div>

</template>

<script>
import Quotes from "./components/QuoteGrid.vue"
import newQuote from"./components/newQuote.vue"
import header from "./components/header.vue"
export default {
  data:()=>{
    return {
      maxQuote:10,
      quotes:['This is for the View',"this is the 2nd "]
    }
  },components:{
    gQuotes:Quotes,
    nQuote:newQuote,
    pHead:header
  },
  methods:{
    added(quote){
      this.quotes.push(quote)
    },
    deletethis(index){
      this.quotes.splice(index,1)
    }
  }
}
</script>

<style lang="scss">

</style>
