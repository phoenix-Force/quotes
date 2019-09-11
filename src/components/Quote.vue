<template>
  <div class="col-sm-6 col-md-4 col-lg-3">
    <div class="panel panel-default">
      <div class="panel-body quote">
        <slot>

        </slot>

      </div>
    </div>

  </div>

</template>
<script>
export default {

}
</script>
<style scoped>
.panel-body{
  font-size: 24px;
  font-family:'Indie Flower', cursive;
  color:#000000;

}
.quote{
  background-color:#d7f4fb;
  cursor: pointer;

}
.quote:hover{
  background-color:#a5262e;
  color:white;
}
</style>
