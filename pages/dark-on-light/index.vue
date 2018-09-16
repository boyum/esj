<template>
  <div class="home">
    <div class="container">
      <h1>Emilie Sofie Johannesen</h1>
      <nav><ul>
        <li>
          <nuxt-link to="/dark-on-light">Home</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/dark-on-light/contact">Contact</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/dark-on-light/cv">CV</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/dark-on-light/photos">Photos</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/">Back</nuxt-link>
        </li>
      </ul></nav>
      <div class="img">
        <img src="/emilie-coffee.jpg" alt="">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  
}
</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css?family=Playfair+Display');
.home {
  background-color: #f2f2f2;
  display: flex;
  min-height: 100vh;
  justify-content: center;
  padding: 2rem 0;

  @media screen and (min-width: 800px) {
    padding: 4rem 0;
  }
}

.container {
  background-color: #ffffff;
  border: 3px solid #eee;
  border-radius: 3px;
  max-width: 1200px;
  padding: 2rem;
  width: 90%;
}
h1 {
  font-family: 'Playfair Display', serif;
  font-size: 4rem;
  font-weight: 100;
  margin: 5rem 0 4rem;
  text-align: center;
}

ul {
  display: flex;
  justify-content: space-around;
  list-style: none;
  margin: 0;
  padding: 0 32%;
  position: relative;

  &::before,
  &::after {
    background-color: #eee;
    content: '';
    height: 2px;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    width: 30%;
  }

  &::before {
    left: 0;
  }
  &::after {
    right: 0;
  }
}

h1,
li a {
  color: #333; 
}

li a {
  border-bottom: 2px solid transparent;
  font-size: 1rem;
  letter-spacing: .05em;
  text-decoration: none;
  text-transform: uppercase;
  transition: border-bottom-color .15s ease-in-out;

  &.nuxt-link-exact-active {
    border-bottom-color: #eee;
  }
  &:hover,
  &:focus {
    border-bottom-color: currentColor;
  }

}

.img {
  margin-top: 5rem;
  img {
    display: block;
    margin: 0 auto;
    max-width: 500px;
  }
}
</style>

