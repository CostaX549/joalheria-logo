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
import product1Image from '../assets/images/product1.png';
import jewerlyProduct2Image from '../assets/images/jewerlyproduct02.png';
import jewerlyProduct3Image from '../assets/images/jewerlyproduct03.png';
import jewerlyProduct4Image from '../assets/images/jewerlyproduct04.png';
import jewerlyProduct5Image from '../assets/images/jewerlyproduct05.png';
import jewerlyProduct6Image from '../assets/images/jewerlyproduct06.png';
import jewerlyProduct7Image from '../assets/images/jewerlyproduct07.png';
import jewerlyProduct8Image from '../assets/images/jewerlyproduct08.png';

const products = ref([
  { name: 'Gemstone', price: '20000', image: product1Image, avaliacao: 5.0 },
  { name: 'Gold Necklace', price: '10000', image: jewerlyProduct2Image, avaliacao: 5.0 },
  { name: 'Gold Choker Set', price: '30000', image: jewerlyProduct3Image, avaliacao: 5.0 },
  { name: 'Jewelry Ring', price: '80000', image: jewerlyProduct4Image, avaliacao: 5.0 },
  { name: 'Jewelry Bangle', price: '5000', image: jewerlyProduct5Image, avaliacao: 5.0 },
  { name: 'Jewelry Necklace Espiral', price: '5000', image: jewerlyProduct6Image, avaliacao: 5.0 },
  { name: 'Jewelry Esmerald Necklace', price: '20000', image: jewerlyProduct7Image, avaliacao: 5.0 },
  { name: 'Jewelry Gold Earrings', price: '15000', image: jewerlyProduct8Image, avaliacao: 5.0 },
]);

</script>

