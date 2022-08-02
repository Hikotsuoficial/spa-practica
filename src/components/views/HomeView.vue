<template>
  <div class="theme-green">
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
    <div class="info-section">
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
@import "@/assets/styles/main.scss";

.aside_menu {
  height: 100vh;
  width: 18vw;
  background: var(--color-wall-1);
  position: fixed;
}

.main__nav {
  height: 100%;
  width: 100%;
  display:flex;
  justify-content: center;
  align-items: center;
}
.info-section {
  margin-left: 18vw;
  height: 100vh;
  width: 82vw;
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
  color: var(--font-color-2);
  background-color: var(--color-wall-3);
}
.wall__content {
  border: var(--box-viewer);
  width: 60%;
}
</style>
