<template>
  <div>
    <p class="grettings">Hola, mi nombre es</p>
    <!-- <img class="photo-perfil" src="@/assets/media/img/photo-perfil.jpg" alt=""> -->
  </div>
  <div class="wall-item-first">
    <h1 class="title-text">Erisc</h1>
    <p class="text-description">
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nobis error dicta incidunt
      doloremque rem magnam consectetur earum tempore obcaecati suscipit omnis ducimus, explicabo,
      perspiciatis ratione accusantium tempora quam, dolorem voluptatibus!
    </p>
    <button class="btn-wellcome">Disfruta mi web!</button>
  </div>
</template>

<style lang="scss" scoped>
@import '@/assets/styles/main.scss';
.grettings{
  font-family: var(--font-mono);
  font-size: 1rem;
  letter-spacing: -0.2px;
}
.wall-content .wall-item-first{

  @media screen and (max-width: 320px) {
    transition:0.2s;
    width: 90%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
}

.title-text {
  font-size: 5.5rem;
  font-weight:700;
  letter-spacing: -2px;
  @include reset-padding-margin();
}

.text-description{
width: 60%;
letter-spacing: 0.2px;
color: var(--font-color-2);

  @media screen and (max-width: 768px) {
    transition:0.2s;
    width: 90%;
  }

  @media screen and (max-width: 425px) {
    transition:0.2s;
    width: 90%;
  }

  @media screen and (max-width: 320px) {
    transition:0.2s;
    width: 100%;
  }
}
.btn-wellcome{
  margin: 20px 0;
  height: 60px;
  width: 18%;
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

  @media screen and (max-width: 768px) {
    transition:0.2s;
    width: 40%;
  }

  @media screen and (max-width: 320px) {
    transition:0.2s;
    width: 60%;
  }
}
</style>
