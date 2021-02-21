<template>
  <div class="hello">
        <b-card
          bg-variant="light"
          :header="nameProduct"
          align="center"
          style="height: 35rem"
        >
          <b-card-img :src="img"></b-card-img>
          <b-card-text><h4> ราคา : {{ price }} </h4></b-card-text>
         
           <b-button variant="primary" @click="buyClick">
                Buy  จำนวน <b-badge variant="light"
                  >{{ like
                  }}<span class="sr-only"></span></b-badge
                >
              </b-button>
        </b-card>
  </div>
</template>
<script>
export default {
  props: {
    img: String,
    price: Number,
    nameProduct: String
  },
  data() {
    return {
      like: 0,
    };
  },
   methods: {
    buyClick(){
      this.like++,
      this.$emit("callbackLike", this.price);      
    }
  }
};
</script>
