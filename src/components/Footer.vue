<template>
  <div class="social-float-wrapper">
    <ul class="social-list">
      <li class="social-item"><v-icon>mdi-github-circle</v-icon></li>
      <li class="social-item"><v-icon>mdi-linkedin-box</v-icon></li>
      <li class="social-item"><v-icon>mdi-instagram</v-icon></li>
    </ul>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.social-float-wrapper {
  width: 40px;
  position: fixed;
  bottom: 0px;
  left: 40px;
  z-index: 10;

  .social-list {
    display: flex;
    flex-direction: column;
    -moz-box-align: center;
    align-items: center;
    padding: 0px;
    margin: 0px;
    list-style: outside none none;
    .social-item {
      .v-icon {
        display: inline-block;
        text-decoration: none;
        text-decoration-skip-ink: auto;
        position: relative;
        transition: all 0.25s cubic-bezier(0.645, 0.045, 0.355, 1) 0s;
        cursor: pointer;
      }
      margin-top:10px;   
      &:last-of-type {
        margin-bottom: 20px;
      }
    }
    &:after {
      content: "";
      display: block;
      width: 1px;
      height: 90px;
      margin: 0px auto;
      background-color: rgb(168, 178, 209);
    }
  }
}
</style>
