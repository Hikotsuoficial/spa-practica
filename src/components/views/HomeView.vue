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
      <div class="social-media-container">
        <p>comida para palomas</p>
      </div>
      <div class="wall-1" id="wellcome">
        <section class="wall-content">
          <div>
            <p class="grettings">Hola, mi nombre es</p>
            <!-- <img class="photo-perfil" src="@/assets/media/img/photo-perfil.jpg" alt=""> -->
          </div>
          <div class="wall-item-first">
          <h1 class="title-text">Erisc</h1>
          <p class="text-description">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nobis error dicta incidunt
            doloremque rem magnam consectetur earum tempore obcaecati suscipit omnis ducimus,
            explicabo, perspiciatis ratione accusantium tempora quam, dolorem voluptatibus!
          </p>
          <button class="btn-wellcome">Disfruta mi web!</button>
          </div>

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
          <ContactForm></ContactForm>
        </section>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import ContactForm from '@/components/molecules/ContactForm.vue';

export default defineComponent({
  name: 'HomeView',
  components: {
    ContactForm,
  },
});
</script>

<style lang="scss">
@import "@/assets/styles/main.scss";

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
    transition: 0.3s;

  }
}

.main-menu .nav-link {
  // margin-left: 3rem;
  text-align: right;
  // text-shadow: var(--text-shadow-1);
  transition: 0.3s;
  padding: 18px;

  &:hover {
    background: linear-gradient(
      90deg,
      rgba(13, 33, 59, 1) 0%,
      rgba(34, 37, 41, 1) 50%,
      rgba(34, 37, 41, 1) 100%
    );
  transition: background 0.3s;
  }

  @media screen and (max-width: 1440px) {
  }

  @media screen and (max-width: 1024px) {
    font-weight: 600;

    &:hover{
    background: none;
    border-bottom: 0;
    }

  &:active{
      background: linear-gradient(
      90deg,
      rgba(13, 33, 59, 1) 0%,
      rgba(34, 37, 41, 1) 50%,
      rgba(34, 37, 41, 1) 100%
    );
  }
  }
}

.nav-link a {
  font-family: var(--font-mono);
  font-weight: 700;
  text-decoration: none;
  color: var(--font-color-1);
  // position: relative;
  font-size: 1rem;
  letter-spacing: 0.5px;

  @media screen and (max-width: 1024px) {

  font-size: 1rem;
  position: relative;
  letter-spacing: 0.7px;

  &:before {
    content: "";
    background: linear-gradient(
      90deg,
      rgba(36, 104, 143, 1) 0%,
      rgba(51, 54, 58, 1) 50%,
      rgba(51, 54, 58, 1) 100%
    );
    position: absolute;
    height: 5px;
    width: 0;
    right: 0px;
    bottom: -12px;
    transition: 0.3s;
  }

  &:hover::before {
    width: 100%;
  }

  }

  @media screen and (max-width: 768px) {
    font-size: 1rem;
  }
}

.info-section {
  margin-left: 20%;
  height: 100vh;
  z-index: 10;

  @media screen and (max-width: 1440px) {
    transition:0.3s;
  }

  @media screen and (max-width: 1024px) {
    margin-left: 0;
    transition:0.3s;
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
  display: flex;
  flex-direction: column;
  padding: var(--padding-boxes);
  border-radius: var(--border-radius);
  // box-shadow: var(--box-shadow);
  // border: var(--box-viewer);

  @media screen and (max-width: 1024px) {
    transition:0.2s;
  }

  @media screen and (max-width: 768px) {
    transition:0.2s;
  }
}

.wall-content .photo-perfil{
  width: 220px;
  border-radius: 50%;
  border: 5px solid whitesmoke;
}

.grettings{
  font-family: var(--font-mono);
  font-size: 1rem;
  letter-spacing: -0.2px;
}

.title-text {
  font-size: 5.5rem;
  font-weight:700;
  letter-spacing: -2px;
  @include reset-padding-margin();
}

.subtitle-text {
  font-size: 1rem;
}

.text-description{
width: 60%;
letter-spacing: 0.2px;
color: var(--font-color-2);

}

.btn-wellcome{
  margin: 20px 0;
  height: 60px;
  padding: 0 30px;
  background: none;
  font-weight: 700;
  font-size: 1rem;
  color: var(--color-wall-3);
  border: 2px solid var(--color-wall-3);
  border-radius: var(--border-radius);
  font-family: var(--font-mono);

  &:hover{
    background: var(--btn-hover-color);
  }
}
// SEccion social media

.social-media-container{
  position:absolute;
  height: 60px;
  color: var(--font-color-2)
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
