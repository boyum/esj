
<template>
  <div class="container">
    <div class="left">
      <h1>Emilie Sofie Johannesen</h1>
      <nav>
        <ul>
          <li>
            <nuxt-link to="/casting-moscow">Home</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/casting-moscow/contact">Contact</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/casting-moscow/cv">CV</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/casting-moscow/photos">Photos</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/">Back</nuxt-link>
          </li>
        </ul>  
      </nav>
    </div>
    <div class="right">
      <carousel :per-page="1" :pagination-enabled="true" :loop="true"> 
        <slide>
          <div class="carousel-image carousel-image--1"></div>
        </slide>
        <slide>
          <div class="carousel-image carousel-image--2"></div>
        </slide>
        <slide>
          <div class="carousel-image carousel-image--3"></div>
        </slide>
      </carousel>
    </div>
  </div>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel';
export default {
  components: {
    Carousel,
    Slide
  }
};
</script>

<style lang="scss">
.container {
  align-items: stretch;
  display: flex;
  flex-direction: column;
  min-height: 100vh;

  @media screen and (min-width: 400px) {
    flex-direction: row;
  }
}
h1,
nav a {
  color: #f2f2f2;
}
h1 {
  font-size: 3rem;
  margin-top: 14rem;
}
nav ul {
  display: flex;
  flex-wrap: wrap;
  line-height: 2;
  margin: 1.5rem 0 0;
  padding: 0;

  li {
    margin-right: 1.5rem;
  }

  a {
    font-size: 1.2rem;
  }
}
.left {
  background-color: #222;
  padding: 5rem 2rem;
  width: 400px;
}
.right {
  background-color: #f2f2f2;
  position: relative;
  width: calc(100% - 400px);

  &::before {
    background-image: linear-gradient(to right, #222, rgba(#222, 0) 30%);
    bottom: 0;
    content: '';
    left: 0;
    pointer-events: none;
    position: absolute;  
    right: 0;
    top: 0;
    z-index: 1;
  }
}

.VueCarousel {
  width: 100%;
}
.carousel-image {
  background-position: 50% 50%;
  background-repeat: no-repeat;
  background-size: cover;
  height: 100vh;
}

.carousel-image--1 {
  background-image: url('/emilie-coffee.jpg');
}
.carousel-image--2 {
  background-image: url('/emilie-headshot.jpg');
}
.carousel-image--3 {
  background-image: url('/emilie-headshot.jpg');
}

.VueCarousel-pagination {
  position: absolute; 
  right: 2%;
  top: 50%;
  transform: translateY(-50%);
  width: auto !important;
  z-index: 1;
}

.VueCarousel-dot-container {
  background-color: #222;
  border-radius: 60px;
  position: absolute;
  top: 50%;
  right: 2%;
  transform: translateY(-50%);
}

.VueCarousel-dot {
  display: block !important;
  margin-top: 0 !important;

  button {
    background-color: #fff !important;
  }
}

.VueCarousel-dot--active {
  button {
    background-color: rgb(15, 97, 26) !important;
  }
}
</style>

