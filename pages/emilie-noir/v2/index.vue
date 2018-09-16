<template>
  <div class="home">
    <div class="container">
      <h1>Emilie Sofie Johannesen</h1>
      <div class="social-media">
        <a href="https://www.instagram.com/msemiliesofie" target="_blank" rel="noopener noreferrer"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-instagram"><rect x="2" y="2" width="20" height="20" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" y1="6.5" x2="17.5" y2="6.5"/></svg><span>Instagram</span></a>
        <a href="https://twitter.com/msemiliesofie" target="_blank" rel="noopener noreferrer"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-twitter"><path d="M23 3a10.9 10.9 0 0 1-3.14 1.53 4.48 4.48 0 0 0-7.86 3v1A10.66 10.66 0 0 1 3 4s-4 9 5 13a11.64 11.64 0 0 1-7 2c9 5 20 0 20-11.5a4.5 4.5 0 0 0-.08-.83A7.72 7.72 0 0 0 23 3z"/></svg><span>Twitter</span></a>
      </div>
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
export default {};
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
  margin: 10rem 0 4rem;
  max-width: 400px;
}

ul {
  display: flex;
  flex-wrap: wrap;
  line-height: 2;
  list-style: none;
  margin: 0;
  max-width: 400px;
  padding: 0;
  position: relative;
  &::before {
    left: 0;
  }
  &::after {
    right: 0;
  }
}
li {
  margin-right: 1.5rem;
}
a {
  border-bottom: 2px solid transparent;
  color: #ddd;
  font-size: 1.5rem;
  letter-spacing: 0.05em;
  text-decoration: none;
  transition: border-bottom-color 0.15s ease-in-out;

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
    height: 650px;
    margin: 0 auto;
    max-height: 90%;
    position: absolute;
    right: 0;
  }
}

.social-media {
  margin: -3rem 0 3rem;
  a {
    border: 1px solid;
    border-radius: 40px;
    display: inline-block;
    margin-right: 1rem;
    padding: .5rem 1rem;
    svg {
      margin-right: .5em;
      vertical-align: sub;
    }
  }
}
</style>

