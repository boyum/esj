<template>
  <div class="container">
    <div>
      <h1 class="title">
        esj
      </h1>
      <div class="links">
        <nuxt-link to="/emilie-noir/v1" class="button--green">Version 1</nuxt-link>
        <nuxt-link to="/emilie-noir/v2" class="button--green"> Version 2</nuxt-link>
      </div>
    </div>
  </div>

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

