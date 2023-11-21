<template>
    <div id="tree-directory"></div>
    <div id="person-card"></div>
    <div id="info-bg">
      <main id="info-box">
      
      </main> 
    </div>
     
</template>

<script setup>

</script>

<style scoped lang="scss">
#info-bg{
  position: absolute;
  width: 100%;
  height: 100%;
  left: 0;
  top: 0;
}
#info-box{
  background-color: aqua;
  min-height: 100%;
  min-width: 648px;
  width: 50%;
  margin: 0 auto;
}
#tree-directory{
  background-color: aquamarine;
}
#person-card{
  background-color: antiquewhite;
}
</style>
