<template>
  <div class="home">
    <div class="container">
      <h1>Emilie Sofie Johannesen</h1>
      <nav><ul>
        <li>
          <nuxt-link to="/emilie-noir">Home</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/emilie-noir/contact">Contact</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/emilie-noir/cv">CV</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/emilie-noir/photos">Photos</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/">Back</nuxt-link>
        </li>
      </ul></nav>
      <div class="img">
        <img src="/emilie-headshot-fixd3.png" alt="">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  
}
</script>

<style lang="scss" scoped>
.home {
  background-color: #000;
  display: flex;
  min-height: 100vh;
  justify-content: center;
  padding: 2rem 0;

  @media screen and (min-width: 800px) {
    padding: 4rem 0;
  }
} 

.container {
  max-width: 1200px;
  padding: 2rem;
  position: relative;
  width: 90%;
}
h1 {
  color: #ddd;
  font-size: 4rem;
  font-weight: 700;
  margin: 5rem 0 4rem;
  width: 400px;
}

ul {
  list-style: none;
  margin: 0;
  padding: 0;
  position: relative;
  &::before {
    left: 0;
  }
  &::after {
    right: 0;
  }
}

li a {
  border-bottom: 2px solid transparent;
  color: #ddd;
  font-size: 1.5rem;
  letter-spacing: .05em;
  text-decoration: none;
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
    bottom: 0;
    display: block;
    filter: grayscale(100%);
    height: 600px;
    margin: 0 auto;
    max-height: 90%;
    position: absolute;
    right: 0;
  }
}
</style>

