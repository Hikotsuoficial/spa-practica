<template>
  <div class="theme-blue">
    <aside class="aside-menu">
      <nav class="main-nav">
      <div id="toogle-menu" class="toogle-menu">
        <!-- <img src="@/assets/media/img/logo.png" alt=""> -->
      </div>
        <ul id="main-menu" class="main-menu">
          <li class="nav-link"><a href="#wellcome">BIENVENIDO</a></li>
          <li class="nav-link"><a href="#cards">QUIEN SOY</a></li>
          <li class="nav-link"><a href="#whatwedo">QUE HAGO</a></li>
          <li class="nav-link"><a href="#contact">HACEMOS UN PROYECTO?</a></li>
        </ul>
      </nav>
    </aside>
    <div class="info-section">
      <!-- <div class="social-media-container">
        <p>comida para palomas</p>
      </div> -->
      <div class="wall-1" id="wellcome">
        <section class="wall-content">
          <WellCome></WellCome>
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
import WellCome from '@/components/molecules/WellCome.vue';

export default defineComponent({
  name: 'HomeView',
  data() {
    return {
      show: 'main-menu',
    };
  },
  components: {
    ContactForm, WellCome,
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

  @media screen and (max-width: 320px) {
    transition: 0.2s;
    position: block;
  }
}

.main-nav {
  height: 100%;
  width: 100%;
  @include center-items();
  // justify-content: flex-end;
  @media screen and (max-width: 320px) {
    transition: 0.2s;
  }
}

.toogle-menu{
  width: 40px;
  position: absolute;
  top: .6rem;
  right: .6rem;
  cursor: pointer;
  z-index: 1;

  @media screen and (min-width: 768px) {
    display: none;
    transition: 0.2s;
  }
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

  @media screen and (max-width: 320px) {
    display: flex;
    flex-direction: column;
    justify-content:center;
    align-items: center;
    margin:0;
    transition: 0.3s;
    transform: translateY(-100%);
  }
}

.main-menu--show{
  transform: translateY(0);
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

  @media screen and (max-width: 320px) {
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

  @media screen and (max-width: 425px) {
    transition:0.2s;
    width: 90%;
  }

  @media screen and (max-width: 320px) {
    transition:0.2s;
    width: 90%;
    text-align: center;
  }
}

.wall-content .photo-perfil{
  width: 220px;
  border-radius: 50%;
  border: 5px solid whitesmoke;
}

.subtitle-text {
  font-size: 1rem;
}

// SEccion social media

.social-media-container{
  position:fixed;
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
