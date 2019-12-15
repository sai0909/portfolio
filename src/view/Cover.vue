<template>
  <div class="cover-bg" :class="toggleBg">
    <v-container>
      <div class="fluid-xy fluid-padding">
        <h2>
          Hello, I'm
          <span
            
            >Sai Venkatesh</span
          >
        </h2>
        <h1>
          A front-end developer / creative customizer who loves creating things
          that are beautiful and functional.
        </h1>
      </div>
    </v-container>
  </div>
</template>
<script>
export default {
  props:['darkTheme'],
  computed:{
    toggleBg: function(){
      return this.darkTheme ? 'moon-light':'sun-light'
    }
  }
};
</script>
<style lang="scss" scoped>


// .moon-light{
//   &:before{
//     background:#000;
//     opacity: 0.6;
//     position: absolute;
//     content: "";
//     width: 100%;
//     height: 100%;
//     left: 0;
//     top: 0;
//   }
// }

// .sun-light{
//   &:before{
//     background:#eee;
//     opacity: 0.6;
//     position: absolute;
//     content: "";
//     width: 100%;
//     height: 100%;
//     left: 0;
//     top: 0;
//   }
// }

</style>
