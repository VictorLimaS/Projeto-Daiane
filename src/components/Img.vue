<template>
  <img :src="imagemSrc" alt="Imagem">
</template>

<script>
export default {
  name: 'Img',
  data() {
    return {
      imagemSrc: 'src/assets/img/perfil.png',
    };
  }
};
</script>

<style scoped>
img {
  height: 100%;
  width: 100%;
  object-fit: cover; 
  object-position: center;

}
  
</style>