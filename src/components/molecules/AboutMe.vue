<template>
  <h1 class="title-text">Quien soy</h1>
  <div class="card-container-section">
    <section class="card-item-1">
      <p class="personal-description">
        Soy una persona que disfruta la programación especialmente en su lado visual, haciendo que
        los usuarios tengan una experiencia agradable. Mi gusto por el desarrollo comenzó en el
        2019, donde creé paginas estáticas usando HTML y CSS.
      </p>
      <p class="personal-description">
        En la actualidad aun sigo estudiando, y he realizando varios cursos donde he ido mejorando
        mis habilidadas y ampliando la gama de plataformas en las cuales se desarrolla contenido
        Front-End.
      </p>
    </section>
    <section class="card-item-2">
      <img class="perfil-pic" src="@/assets/media/img/photo-perfil.jpg" alt="" />
      <div class="perfil-pic-background"></div>
    </section>
    <section class="card-item-3">
      <h2 class="title-text">Skills</h2>
      <div class="list-skills">
        <div>
          <ul>
            <li>HTML</li>
            <li>JavaScript (ES6+)</li>
            <li>CSS</li>
          </ul>
        </div>
        <div>
          <ul>
            <li>Grid CSS</li>
            <li>FlexBox</li>
            <li>VueJS</li>
          </ul>
        </div>
      </div>
    </section>
  </div>
</template>

<style lang="scss" scoped>
@import "@/assets/styles/main.scss";

.card-container-section {
  padding: var(--padding-boxes-2);
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: 1fr 1fr;
  justify-content: center;
  gap: var(--padding-boxes-1);
  color: var(--font-color-2);
  width: 84%;
  z-index: 1;

  @media screen and (max-width: 1024px) {
    grid-template-columns: repeat(2, 1fr);
    width: 100%;
  }
}

.personal-description {
  font-size: 1rem;
  padding: var(--padding-boxes-1);
}

.card-item-1,
.card-item-2,
.card-item-3 {
  padding: var(--padding-boxes-1);
}

.card-item-1,
.card-item-3 {
  grid-column-start: 1;
  grid-column-end: 2;
}

.card-item-2 {
  grid-row-start: 1;
  grid-row-end: 3;
  grid-column-start: 2;
  grid-column-end: 3;
  @include center-items();
}

.card-item-3 {
  display: flex;
  flex-direction: column;
  margin: 10px;
  padding: var(--padding-boxes-2);
}

.list-skills {
  margin-left: 20px;
  margin-top: 10px;
  display: grid;
  grid-template-columns: 50% 50%;
  grid-template-rows: 1fr;
  font-family: var(--font-mono);
  font-size: 0.8rem;
}

.list-skills ul {
  list-style: none;
}

.list-skills ul li {
  padding: 3px 0px;

  &::before {
  content: "\0025B9";
  margin-left: -20px;
  margin-right: 10px;
  color: var(--color-wall-3)
}
}

.perfil-pic {
  width: 280px;
  border-radius: 20% 70% 70% 30% / 30% 30% 70% 70%;
  z-index: 2;
}

.perfil-pic-background {
  position: absolute;
  width: 280px;
  height: 280px;
  background-color: var(--color-wall-1);
  border-radius: 20% 70% 70% 30% / 30% 30% 70% 70%;
  transform: rotateZ(-50deg);
  transition: background-color 0.3s;
}
</style>
