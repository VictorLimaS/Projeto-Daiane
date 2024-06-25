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
        <Input text="WHATSAPP" :url="'https://api.whatsapp.com/send?phone=5513991580976'" />
        <Input text="INSTAGRAM" :url="'https://www.instagram.com/daianepereirapmu/'" />
        <Input text="FACEBOOK" :url="'https://www.facebook.com/dannepereiraa'" />
      </div>
      <div class="social">
        <i class="bi bi-instagram icon" @click="redirectTo('https://www.instagram.com/daianepereirapmu/')"
           @mouseover="hoverEffect('instagram')" @mouseleave="resetColor('instagram')"></i>
        <i class="bi bi-whatsapp icon" @click="redirectTo('https://api.whatsapp.com/send?phone=5513991580976')"
           @mouseover="hoverEffect('whatsapp')" @mouseleave="resetColor('whatsapp')"></i>
        <i class="bi bi-facebook icon" @click="redirectTo('https://www.facebook.com/dannepereiraa')"
           @mouseover="hoverEffect('facebook')" @mouseleave="resetColor('facebook')"></i>
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
    default:
      break;
  }
};

const redirectTo = (url) => {
  window.open(url, '_blank');
};
</script>

<style scoped>
.home {
  display: flex;
  align-items: center;
  width: 100%;
  height: 100%;
  padding: 2rem;
  gap: 2rem;
  margin-top: 3rem;
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
  color: white;
  margin-bottom: 2rem
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
    padding: 0 1rem
  }

  .img {
    width: 18rem;
    height: 18rem;
    border-radius: 50%;
    overflow: hidden;
  }

  .name {
  margin-bottom: 0rem
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

  .social {
    font-size: 3rem;
    margin-top: 1rem;
  }
}

@media (max-width: 700px) {
  .img {
    width: 10rem;
    height: 10rem;
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
  }

  .label {
    padding: 0 .3rem;
  }
}

@media (max-width: 500px) {
  h1 {
    font-size: 2.3rem;
  }

  h3 {
    font-size: 1.1rem;
  }
}
</style>
