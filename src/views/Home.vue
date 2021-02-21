<template>
  <div class="home">
    <b-container>
      <div class="mt-3">
    <b-card-group deck>
      <b-card bg-variant="light" header="Total product price" class="text-center">
      
        <b-card-text><h3>฿{{ totalLike }}</h3></b-card-text>
        <b-button variant="success" v-on:click="say" @click="CancelAllItem"
      >Buy</b-button
    >
    
      </b-card>
    </b-card-group>
    
  </div>
      <br />
      <b-row>
        <b-col cols="4" v-for="index in productList" :key="index">
          <Product
            :img="index.img"
            :price="index.price"
            :nameProduct="index.nameProduct"
            @callbackLike="likelike"
          />
         
        </b-col>
      </b-row>
      <div class="mt-3">
  </div>
    </b-container>
    
  </div>
</template>

<script>
// @ is an alias to /src
import Product from "@/components/product.vue";
export default {
  name: "Home",
  props: {
    productList: Array
  },
  components: {
    Product
  },
   data() {
    return {
     totalLike: 0,
     like:  0
    };
  },
  methods: {
    say: function () {
      if (this.totalLike != 0) {
        alert("ส่งซื้อสินค้าเรียบร้อย");
      } else if (this.totalLike <= 0) {
        alert("กรุณาเลือกสินค้า");
      }
    },
    likelike(value){
         this.totalLike += value;
    },
    CancelAllItem() {
      this.totalLike = 0;
      this.like = 0;
      }
      
    },
    
};
</script>
