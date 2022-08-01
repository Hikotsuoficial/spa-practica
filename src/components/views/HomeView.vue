<template>
  <div class="home">
    <aside class="aside_menu">
      <nav class="main__nav">
        <ul main="main__menu">
          <li>Bienvenido</li>
          <li>Quien soy</li>
          <li>Que hago</li>
          <li>Hacemos un proyecto?</li>
        </ul>
      </nav>
    </aside>
    <div class="info__section">
      <div class="wall-1">
        <section class="wall__content">
          <p>Hi! my name is Erisc Valencia Mosquera</p>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nobis error dicta incidunt
            doloremque rem magnam consectetur earum tempore obcaecati suscipit omnis ducimus,
            explicabo, perspiciatis ratione accusantium tempora quam, dolorem voluptatibus!
          </p>
        </section>
      </div>
      <div class="wall-2">
        <section class="wall__content">
          <p>Hi! my name is Erisc Valencia Mosquera</p>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nobis error dicta incidunt
            doloremque rem magnam consectetur earum tempore obcaecati suscipit omnis ducimus,
            explicabo, perspiciatis ratione accusantium tempora quam, dolorem voluptatibus!
          </p>
        </section>
      </div>
      <div class="wall-1">
        <section class="wall__content">
          <p>Hi! my name is Erisc Valencia Mosquera</p>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nobis error dicta incidunt
            doloremque rem magnam consectetur earum tempore obcaecati suscipit omnis ducimus,
            explicabo, perspiciatis ratione accusantium tempora quam, dolorem voluptatibus!
          </p>
        </section>
      </div>
      <div class="wall-2">
        <section class="wall__content">
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

<style lang="scss" scoped>
@import '@/assets/styles/main.scss';

// section, div {
//   border: 1px solid gold;
// }

.home {
  display: flex;
}

.aside_menu {
  height: 100vh;
  width: 18vw;
  background: rgb(145, 175, 128);
  position:fixed;
}

.main__nav{

  height: 100%;
  width: 100%;

  display: flex;
  justify-content: center;
  align-items: center;
}

.info__section{
  height: 100vh;
  width: 100vw;
  /* overflow: hidden; */
}

.wall-1, .wall-2 {
  height: 100vh;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.wall__content{
  width: 60%;
  padding: 1rem;
  border: 1px solid red;
}

</style>
