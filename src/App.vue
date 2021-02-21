<template>
  <div id="app">
    <b-navbar toggleable type="dark" variant="dark">
      <b-navbar-brand to="/">Gunpla shop</b-navbar-brand>
     <b-button variant="danger" href="/" @click="CancelAllItem"> Clear product </b-button>
    </b-navbar>

    <router-view :productList="productList"/>
  </div>
</template>

<script>
export default {
  data() {
    return {
      productList: [
        {
          price: 750,
          nameProduct: "BANDAI GUNPLA HIGH EXTREME GRADE HG 1/144 GUNDAM AGE II MAGNUM SV VER",
          img:
            "https://cf.shopee.co.th/file/3aa19bb21b569f1d4c12d074a05e823e"
        },
        {
          price: 2720,
          nameProduct: "BANDAI HIGH GUNPLA MASTER EXTREME MGEX GRADE MG 1/100 00 XN RAISER",
          img:
            "https://cf.shopee.co.th/file/c8ffb951243aab887f0519cb1cf32d82"
        },
        {
          price: 8590,
          nameProduct: "BANDAI GUNPLA MASTER GRADE EXTREME MGEX 1/100 RX-0 UNICORN GUNDAM VER KA",
          img:
            "https://th-test-11.slatic.net/p/46c41041fdbcb98dcd043e62fd7e6f1b.jpg_720x720q80.jpg_.webp"
        },
        {
          price: 410,
          nameProduct: "BANDAI GUNPLA HIGH GRADE HG 1/144 GUNDAM EXIA REPAIR II",
          img:
            "https://cf.shopee.co.th/file/32609cabffa585c00565f53f2c54d167"
        },
        {
          price: 4420,
          nameProduct: "BANDAI GUNPLA HI-RESOLUTION MODEL HIRM 1/100 GOD GUNDAM",
          img: "https://th-test-11.slatic.net/p/f43c0fc7c0edb91b0206735e11b7a8c1.jpg_720x720q80.jpg_.webp"
        },
        {
          price: 5200,
          nameProduct: "BANDAI GUNPLA MASTER GRADE MG 1/100 FA-010A FAZZ VER KA",
          img: "https://th-test-11.slatic.net/p/02530a548eb8b4af3deb9829f582f118.jpg_720x720q80.jpg_.webp"
        },
        
      ],
    };
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
