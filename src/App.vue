<template>
  <main>
    <ix-header :links="links" />
    <router-view class="container px-5 sm:px-20 py-20 flex justify-center" />
    <ix-footer />
  </main>
</template>

<script>
import IxHeader from "@/components/IxHeader";
import IxFooter from "@/components/IxFooter";

export default {
  name: "App",
  components: { IxHeader, IxFooter },


  data() {
    return {
      links: [
        {
          title: 'BTC',
          to: { name: 'coin-detail', params: { id: 'bitcoin' } }
        },
        {
          title: 'ETH',
          to: { name: 'coin-detail', params: { id: 'ethereum' } }
        },
        {
          title: 'BNB',
          to: { name: 'coin-detail', params: { id: 'binance-coin' } }
        }
      ]
    }
  },

  // watch: {
  //       $route: {
  //           immediate: true,
  //           handler(to, from) {
  //               document.title = to.meta.title || 'Some Default Title';
  //           }
  //       },
  //   }


};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
