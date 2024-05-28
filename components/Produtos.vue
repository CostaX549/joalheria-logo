<template>
    <div id="produtos" class="pt-24">
        <div class="text-[40px] mb-2 text-center font-bold text-white">
            Produtos
        </div>
        <div class="flex justify-center mt-4">
    <div class="grid 2xl:grid-cols-4 xl:grid-cols-3 lg:grid-cols-3 md:grid-cols-3 sm:grid-cols-2 grid-cols-1 gap-4">
        <ProdutoItem v-for="produto in products" :key="produto.name" :produto="produto" />
    </div>
  </div>
    </div>

</template>

<script setup>
const products = ref([
    { name: 'Gemstone', price: '20000', image: '/_nuxt/assets/images/product1.png', avaliacao: 5.0 },
    { name: 'Gold Necklace', price: '10000', image: '/_nuxt/assets/images/jewerlyproduct02.png', avaliacao: 5.0 },
    { name: 'Gold Choker Set', price: '30000', image: '/_nuxt/assets/images/jewerlyproduct03.png', avaliacao: 5.0},
    
    { name: 'Jewerly Ring', price: '80000', image: '/_nuxt/assets/images/jewerlyproduct04.png', avaliacao: 5.0},
    { name: 'Jewerly Bangle', price: '5000', image: '/_nuxt/assets/images/jewerlyproduct05.png', avaliacao: 5.0},
    { name: 'Jewerly Necklace Espiral', price: '5000', image: '/_nuxt/assets/images/jewerlyproduct06.png', avaliacao: 5.0},
    { name: 'Jewerly Esmerald Necklace', price: '20000', image: '/_nuxt/assets/images/jewerlyproduct07.png', avaliacao: 5.0},
    { name: 'Jewerly Gold Earrings', price: '15000', image: '/_nuxt/assets/images/jewerlyproduct08.png', avaliacao: 5.0},
    ])
</script>

