<template>
  <section class="container">
    <div>
      <h1 class="title">
        esj
      </h1>
      <div class="links">
        <nuxt-link to="/dark-on-light"
          class="button--green">Dark on light</nuxt-link>
        <nuxt-link to="/emilie-noir"
          class="button--green">Emilie Noir</nuxt-link>
        <nuxt-link to="/casting-moscow"
          class="button--green">Casting Moscow</nuxt-link>
        <nuxt-link to="/adrianne"
          class="button--green">Adrianne</nuxt-link>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.links {
  padding-top: 15px;

  a+a {
    margin-left: 1rem;
  }
}
</style>

