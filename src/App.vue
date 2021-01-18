<template>
  <div id="nav">
    <navigation>
      
    </navigation>
  </div>
  <router-view/>
</template>

<script>
  import Navigation from '@/components/Navigation'
  export default {
    components: {
      Navigation
    },
  }
</script>
<style lang="stylus">

  $white = rgb(255,255,255)
  $color_accent1 = #4E47DE
  body{
    margin:0;
    
    
  }
 
  .material-icons 
    vertical-align middle
</style>
