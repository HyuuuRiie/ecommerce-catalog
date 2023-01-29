<template>
  <div class="home">
    <ProductDisplay/>
  </div>
</template>

<script>
// @ is an alias to /src
import ProductDisplay from '@/components/ProductDisplay.vue'
import axios from "axios";

export default {
  name: 'HomeView',
  components: {
    ProductDisplay
  },
  data() {
    return {
      mens: [],
    };
  },
  // data yang diambil dari json dimasukkan dalam product
  methods: {
    setProduct(data) {
      this.mens = data;
    },
  },
  mounted() {
    axios
      .get("http://localhost:3000/mens")
      .then((response) =>
        // handle success
        this.setProduct(response.data))
      .catch((error) => console.log(error));
  },
}
</script>
