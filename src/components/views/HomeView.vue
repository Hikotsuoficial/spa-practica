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
        <section class="wall-content">
          <h2 class="subtitle-text">Quien soy</h2>
          <div class="card-container-section">
            <section class="card-item">
              <img src="" alt="" />
            </section>
            <section class="card-item">
              <img src="" alt="" />
            </section>
            <section class="card-item">
              <img src="" alt="" />
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
@import "@/assets/styles/main.scss";

.theme-blue {
  // display: grid;

  // @media screen and (max-width: 1024px) {
  //   grid-template-columns: 1fr;
  // }
  // @media screen and (max-width: 768px) {
  //   grid-template-columns: 1fr;
  // }
  // @media screen and (max-width: 425px) {
  //   grid-template-columns: 1fr;
  // }
  // @media screen and (max-width: 320px) {
  //   grid-template-columns: 1fr;
  // }
}

.aside-menu {
  height: 100vh;
  width: 20%;
  background: var(--color-wall-1);
  position: fixed;
  z-index: 12;

  @media screen and (max-width: 1440px) {
    transition: 0.2s;
  }

  @media screen and (max-width: 1024px) {
    height: 80px;
    width: 100%;
    transition: 0.2s;
  }
}

.main-nav {
  height: 100%;
  width: 100%;
  @include center-items();
  // justify-content: flex-end;
}

.main-menu {
  list-style: none;
  width: 100%;
  // padding: var(--padding-boxes);

  @media screen and (max-width: 1024px) {
    display: flex;
    justify-content:center;
    align-items: flex-end;
  }
}

.main-menu .nav-link {
  // margin-left: 3rem;
  text-align: right;
  font-weight: 700;
  // text-shadow: var(--text-shadow-1);
  padding: 18px;
  border-bottom: 3px solid var(--color-wall-1);
  transition: 0.3s;

  &:hover {
    background: linear-gradient(
      90deg,
      rgba(36, 104, 143, 1) 0%,
      rgba(51, 54, 58, 1) 50%,
      rgba(51, 54, 58, 1) 100%
    );
  }

  @media screen and (max-width: 1024px) {
  &:hover {
    background: linear-gradient(
      180deg,
      rgba(36, 104, 143, 1) 0%,
      rgba(51, 54, 58, 1) 50%,
      rgba(51, 54, 58, 1) 100%
    );
  }
  }
}

.nav-link a {
  text-decoration: none;
  color: var(--font-color-1);
  // position: relative;
  font-size: 1.2rem;
  letter-spacing: 0.6px;

  &::after {
    content: "";
    background: red;
    height: 5px;
    width: 10%;
    right: 0;
    bottom: -10px;
    transition: 0.4s;
  }

  &:after::after {
    width: 100%;
  }

  @media screen and (max-width: 768px) {
    font-size: 1rem;
  }
}

.info-section {
  margin-left: 20%;
  height: 100vh;
  z-index: 10;

  @media screen and (max-width: 1024px) {
    margin-left: 0;
  }
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
  background-color: var(--color-wall-4);
}

.wall-content {
  // border: var(--box-viewer);
  width: 80%;
}

.title-text {
  font-size: var(--titles-big);
  @include reset-padding-margin();
}

.subtitle-text {
  font-size: var(--subttitles);
}

.card-container-section {
  border: var(--box-viewer);
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: 1fr;
  justify-content: center;
  gap: var(--padding-boxes);

  @media screen and (max-width: 1024px) {
    grid-template-columns: repeat(2, 1fr);
  }
  @media screen and (max-width: 768px) {
    grid-template-columns: repeat(2, 1fr);
  }
}

.card-item {
  height: 33%;
  border: var(--box-viewer);
  border-radius: var(--border-radius);
}
</style>
