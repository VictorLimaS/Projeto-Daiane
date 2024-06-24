<template>
  <div class="home">
    <div class="img">
      <Img />
    </div>
    <div class="content">
      <div class="name">
        <h1>Daiane Pereira</h1>
        <h3>@daianepereirapmu</h3>
      </div>
      <div class="label">
        <Input text="WHATSAPP" />
        <Input text="INSTAGRAM" />
        <Input text="TIKTOK" />
      </div>
      <div class="social">
        <i class="bi bi-instagram icon" @mouseover="hoverEffect('instagram')" @mouseleave="resetColor('instagram')"></i>
        <i class="bi bi-whatsapp icon" @mouseover="hoverEffect('whatsapp')" @mouseleave="resetColor('whatsapp')"></i>
        <i class="bi bi-facebook icon" @mouseover="hoverEffect('facebook')" @mouseleave="resetColor('facebook')"></i>
        <i class="bi bi-tiktok icon" @mouseover="hoverEffect('tiktok')" @mouseleave="resetColor('tiktok')"></i>
      </div>
    </div>
  </div>
</template>

<script setup>
import Img from '../components/Img.vue';
import Input from '../components/Input.vue';

const hoverEffect = (platform) => {
  switch (platform) {
    case 'instagram':
      document.querySelector('.bi-instagram').style.color = '#c13584';
      break;
    case 'whatsapp':
      document.querySelector('.bi-whatsapp').style.color = '#25D366';
      break;
    case 'facebook':
      document.querySelector('.bi-facebook').style.color = '#1877f2';
      break;
    case 'tiktok':
      document.querySelector('.bi-tiktok').style.color = 'BLACK';
      break;
    default:
      break;
  }
};

const resetColor = (platform) => {
  switch (platform) {
    case 'instagram':
      document.querySelector('.bi-instagram').style.color = 'white';
      break;
    case 'whatsapp':
      document.querySelector('.bi-whatsapp').style.color = 'white';
      break;
    case 'facebook':
      document.querySelector('.bi-facebook').style.color = 'white';
      break;
    case 'tiktok':
      document.querySelector('.bi-tiktok').style.color = 'white';
      break;
    default:
      break;
  }
};
</script>

<style scoped>
.home {
  display: flex;
  width: 100vw;
  height: 100vh;
  padding: 2rem;
  gap: 2rem;
}

.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
}

.img {
  width: 80%;
}

.name {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 1rem;
  color: white;
}

h1 {
  font-size: 6.7rem;
  font-weight: 300;
  font-family: "Noto Serif", serif;
}

h3 {
  font-size: 2rem;
}

.label {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  gap: 2.3rem;
  padding: 0 5rem;
}

.social {
  display: flex;
  gap: 4rem;
  font-size: 2rem;
  color: white;
  margin-top: 1rem;
}

.social .icon {
  cursor: pointer;
  transition: transform 0.2s ease, color 0.2s ease;
}

.social .icon:hover {
  transform: scale(1.1);
}

@media (max-width: 950px) {
  .home {
    display: inline;
    justify-content: center;
    align-items: center;
  }

  .img {
    width: 20rem;
    height: 20rem;
    border-radius: 50%;
    overflow: hidden;
  }

  .content {
    height: 50%;
  }

  h1 {
    font-size: 5rem;
  }

  .label {
    padding: 0 2rem;
  }

  .name {
    margin-bottom: 5rem;
  }

  .social {
    font-size: 3rem;
    margin-top: 2.5rem;
  }
}

@media (max-width: 700px) {
  .img {
    width: 10rem;
    height: 10rem;
    margin-bottom: 3rem;
  }

  .name {
    margin-bottom: 2rem;
  }

  h1 {
    font-size: 3.1rem;
  }

  h3 {
    font-size: 1.4rem;
  }

  .social {
    font-size: 2rem;
    margin-top: 2.2rem;
  }

  .label {
    padding: 0 .3rem;
  }
}
</style>
