<template>
  <div class="theme-blue">
    <aside class="aside-menu">
      <nav class="main-nav">
        <ul class="main-menu">
          <li class="nav-link"><a href="#wellcome">BIENVENIDO</a></li>
          <li class="nav-link"><a href="#cards">QUIEN SOY</a></li>
          <li class="nav-link"><a href="#whatwedo">QUE HAGO</a></li>
          <li class="nav-link"><a href="#contact">HACEMOS UN PROYECTO?</a></li>
        </ul>
      </nav>
    </aside>
    <div class="info-section">
      <div class="wall-1" id="wellcome">
        <section class="wall-content">
          <h1 class="title-text">Erisc</h1>
          <h2 class="subtitle-text">Valencia Mosquera</h2>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nobis error dicta incidunt
            doloremque rem magnam consectetur earum tempore obcaecati suscipit omnis ducimus,
            explicabo, perspiciatis ratione accusantium tempora quam, dolorem voluptatibus!
          </p>
        </section>
      </div>
      <div class="wall-2" id="cards">
        <section class="wall-content" >
          <h2 class="subtitle-text">Quien soy</h2>
          <div class="card-container-section">
            <section class="card-item">
              <img src="" alt="">
            </section>
            <section class="card-item">
              <img src="" alt="">
            </section>
            <section class="card-item">
              <img src="" alt="">
            </section>
          </div>
        </section>
      </div>
      <div class="wall-1" id="whatwedo">
        <section class="wall-content">
          <p>Hi! my name is Erisc Valencia Mosquera</p>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nobis error dicta incidunt
            doloremque rem magnam consectetur earum tempore obcaecati suscipit omnis ducimus,
            explicabo, perspiciatis ratione accusantium tempora quam, dolorem voluptatibus!
          </p>
        </section>
      </div>
      <div class="wall-2" id="contact">
        <section class="wall-content">
          <p>Hi! my name is Erisc Valencia Mosquera</p>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nobis error dicta incidunt
            doloremque rem magnam consectetur earum tempore obcaecati suscipit omnis ducimus,
            explicabo, perspiciatis ratione accusantium tempora quam, dolorem voluptatibus!
          </p>
        </section>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'HomeView',
});
</script>

<style lang="scss">
@import '@/assets/styles/main.scss';

.theme-blue{
  display: grid;
}

.aside-menu {
  height: 100%;
  width: 20%;
  background: var(--color-wall-1);
  position: fixed;
}

.main-nav {
  height: 100%;
  width: 100%;
  @include center-items();
}

.main-menu{
  list-style: none;
  padding: var(--padding-boxes);

}

.main-menu .nav-link{
  font-size: 1.3rem;
  margin-top: 2.1rem;
  margin-left: 3rem;
  text-align: right;
  font-weight: 700;
  border-bottom:2px solid var(--color-wall-1);
  text-shadow: var(--text-shadow-1);
  padding: 3px;

  &:hover{
    border-bottom:2px solid var(--color-wall-3);
  }
}

.nav-link a{
  text-decoration: none;
  color: var(--font-color-1);
}

.info-section {
  margin-left: 20%;
  height: 100vh;
  width: 80%;
  z-index: 10;
}

.wall-1 {
  height: 100%;
  width: 100%;
  @include center-items();
  color: var(--font-color-1);
  background-color: var(--color-wall-4);
}

.wall-2 {
  height: 100%;
  width: 100%;
  @include center-items();
  color: var(--font-color-1);
  background-color: var(--color-wall-3);
}

.wall-content {
  // border: var(--box-viewer);
  width: 80%;
}

.title-text{
  font-size: var(--titles-big);
  @include reset-padding-margin();
}

.subtitle-text{
  font-size: var(--subttitles) ;
}

.card-container-section{
  border: var(--box-viewer);
  padding: var(--padding-boxes);
  display: grid;
  grid-template-columns: repeat(3, 310px);
  grid-template-rows: 1fr;
  justify-content: center;
  gap: var(--padding-boxes);
}

.card-item{
  height: 250px;
  border: var(--box-viewer);
  border-radius: var(--border-radius);
}

</style>
