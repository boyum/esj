<template>
  <div class="adrianne container">
    <h1>Emilie Sofie Johannesen</h1>
    <span class="subtitle">Actress</span>
    <nav>
      <ul>
        <li>
          <nuxt-link to="/adrienne">Home</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/adrienne/cv">CV</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/adrienne/contact">Contact</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/adrienne/photos">Photos</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/">Back</nuxt-link>
        </li>
      </ul>
    </nav>
    <div class="picture picture-1 drop-left">
      <div></div>
    </div>
    <div class="quote-1">
      <blockquote>
        <p>
          An ne hoc quidem Peripateticis concedis, ut dicant omnium bonorum virorum, id est sapientium omnibusque virtutibus ornatorum, vitam omnibus partibus plus habere semper boni quam mali!
        </p>
        <footer>
          — Lorem Ipsum
        </footer>
      </blockquote>
    </div>

    <div class="bio">
      <div class="left">
        <div class="picture">
          <div></div>
        </div>
      </div>
      <div class="right">
        <h2>Bio</h2>
        <span>About Emilie</span>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Age, inquies, ista parva sunt. Ex rebus enim timiditas, non ex vocabulis nascitur. Sic enim maiores nostri labores non fugiendos tristissimo tamen verbo aerumnas etiam in deo nominaverunt. </p>
        <p>Non est ista, inquam, Piso, magna dissensio. Quae cum praeponunt, ut sit aliqua rerum selectio, naturam videntur sequi; Duo Reges: constructio interrete. </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css?family=Playfair+Display');
.container {
  display: flex;
  flex-direction: column;
  font-family: 'Playfair Display', sans-serif;
  justify-content: center;
  margin: 0 auto;
  max-width: 750px;
  width: 90%;
}
h1,
.subtitle {
  color: #444;
  text-align: center;
}
h1 {
  font-size: 4.5rem;
  font-weight: 900;
  line-height: 1;
  margin: 6rem auto 1rem;
  max-width: 500px;
}

.subtitle {
  font-size: 2.75rem;
  font-weight: 100;
  margin: 0 auto 1rem;
}
nav ul {
  display: flex;
  justify-content: center;
  list-style: none;
  margin: 2rem 0 4rem;
  padding: 0;
}

nav li {
  margin: 0 1rem;
}

nav a {
  color: #444;
  font-size: 1.1rem;
  position: relative;
  text-decoration: none;

  &::after {
    background-color: rgba(55, 85, 135, 0.3);
    bottom: 0;
    content: '';
    height: 0.7em;
    left: 0;
    position: absolute;
    right: 0;
    transform: scaleY(0.2) scaleZ(1);
    transform-origin: 50% 100%;
    transition: transform 0.15s ease-in-out;
  }

  &:hover,
  &:focus {
    &::after {
      transform: scaleY(1) scaleZ(1);
    }
  }
}

.picture {
  position: relative;
  div {
    background-position: 50% 0;
    background-repeat: no-repeat;
    background-size: cover;
    box-shadow: 20px 20px 50px rgba(0, 0, 0, 0.3);
    padding-top: 100%;
    position: relative;
    z-index: 1;
  }

  &::after {
    background-color: #f2f2f2;
    bottom: 0;
    content: '';
    left: 0;
    position: absolute;
    right: 0;
    top: 0;
  }
  &.drop-left {
    &::after {
      transform: translate(-3rem, 3rem);
    }
  }
}
.picture-1 {
  div {
    background-image: url('/emilie-headshot.jpg');
  }
}
.quote-1 {
  margin-top: 10rem;
}

blockquote {
  color: rgba(0, 0, 0, 0.7);
  font-size: 1.9rem;
  font-weight: 600;
  line-height: 1.5;

  &::after {
    clear: both;
    content: '';
    display: table;
  }

  p {
    margin-bottom: 2rem;
  }
  footer {
    float: right;
    font-size: 0.9em;
  }
}

.bio {
  background-color: rgba(55, 85, 135, 0.3);
  display: flex;
  font-size: 1.2rem;
  justify-content: space-between;
  margin-top: 5rem;
  padding: 3rem 2rem;
  .left,
  .right {
    width: 55%;
  }
  .picture {
    transform: translateX(-40%);
    div {
      background-image: url('/emilie-coffee.jpg');
    }
  }
  h2 {
    color: #444;
    font-size: 4rem;
    font-weight: 900;
  }
  span {
    color: rgba(55, 85, 135, 1);
    display: block;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin: 1rem 0;
    text-transform: uppercase;
  }
  p {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }
}
</style>
