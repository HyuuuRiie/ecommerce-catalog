<template>
  <div
    v-bind:class="{
      'page-men': category === 'men’s clothing',
      'page-women': category === 'women’s clothing',
      'page-unavailable':
        category !== 'men’s clothing' && category !== 'women’s clothing',
    }"
  >
    <!-- konten section -->
    <div class="page-men">
      <div class="container">
        <div class="card">
          <div class="img-card">
            <img src="../assets/1.jpg" alt="gambar" class="img">
          </div>
          <div class="title">Men Casual Slim Fit</div>
          <div class="category">men's clothing</div>
          <div class="border"></div>
          <div class="description">great outerwear jackets for Spring/Autumn/Winter, suitable for many occasions, such as working, hiking, camping, mountain/rock climbing, cycling, traveling or other outdoors. Good gift choice for you or your family member. A warm hearted love to Father, husband or son in this thanksgiving or Christmas Day.</div>
          <div class="border2"></div>
          <div class="price">$29.95</div>
          <button class="buy">Buy Now</button>
          <button class="next">Next Product</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductDisplay",
  
};
</script>

<style>
</style>