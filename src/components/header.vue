<template>
<div class="row">
  <div class="col-sm-12">
    <h3>Quote Added</h3>
    <div class="progress">
      <div class="progress-bar" :style="{width:(qCount/Max)*100 +'%'}">
              {{qCount}}/{{Max}}
      </div>
    </div>

  </div>
</div>
</template>
<script>
export default {
  props:['qCount','Max']

}
</script>
<style lang="scss" scoped>

</style>
