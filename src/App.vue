<template>
  <v-app>
    <Header @check-moon="checkMoon"></Header>
    <v-content>
      <Cover :darkTheme="isMoon"></Cover>
      <About></About>
    </v-content>
    <Footer></Footer>
  </v-app>
</template>

<script>
import Header from "./components/Header";
import Cover from "./view/Cover";
import About from "./view/About";
import Footer from "./components/Footer";

export default {
  name: "App",

  components: { Header, Cover, About, Footer },

  data: () => ({
    isMoon: ""
  }),
  methods: {
    checkMoon: function(event) {
      this.isMoon = event;
    }
  }
};
</script>
<style lang="scss">
.fluid-xy {
  margin: 0px auto;
  padding: 150px 30px;
  padding-top: 150px;
  max-width: 1000px;
  display: flex;
  -moz-box-pack: center;
  justify-content: center;
  -moz-box-align: center;
  flex-direction: column;
  align-items: flex-start;
  min-height: 100vh;

  @media (min-width: 1000px) {
    padding: 150px 100px;
  }
}

.p-title {
  @media (max-width: 48em) {
    font-size: 24px;
  }
  content: "";
  position: relative;
  display: flex;
  -moz-box-align: center;
  align-items: center;
  width: 100%;
  white-space: nowrap;
  margin: 10px 0px 40px;
  font-size: 32px;
  &:after {
    content: "";
    background-color: rgb(45, 57, 82);
    margin-left: 20px;
    height: 1px;
    width: 300px;
    display: block;
    position: relative;
  }
}
</style>
