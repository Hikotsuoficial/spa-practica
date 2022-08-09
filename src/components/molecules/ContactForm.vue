<template>
  <h1 class="title-text">Contáctame</h1>
  <div class="form-container">
    <form action="https://formspree.io/f/mgedqodg" method="POST">
      <div class="grid-contact-form">
        <div>
          <label class="label" for="name"
            >Nombre
            <input
              onkeypress="clear()"
              class="contact-input"
              type="text"
              minlength="3"
              name="name"
              maxlength="20"
              required
            />
          </label>
        </div>
        <div>
          <label class="label" for="mail">
            Correo electrónico
            <input class="contact-input" type="email" name="email" required />
          </label>
        </div>
        <div class="textare-message">
          <label class="label" for="message"
            >Mensaje
            <textarea
              class="textarea-msg"
              minlength="20"
              maxlength="400"
              name="message"
              placeholder="Escribe tu mensaje aquí"
              rows="4"
              required
            ></textarea>
          </label>
        </div>
        <button class="btn-send-form" type="submit">Enviar</button>
      </div>
    </form>
  </div>
</template>

<style lang="scss" scoped>
@import '@/assets/styles/main.scss';

.order-form {
  list-style: none;
}
.form-container{
    @media screen and (max-width: 1024px) {
        transition:0.2s;
        width: 100%;
        @include center-items()
      }
}
.label {
  margin: 1rem;
  font-family: var(--font-mono);
}
.contact-input {
  display: block;
  border-radius: var(--border-radius);
  border: 1px solid var(--color-border-1);
  width: 100%;
  height: 3rem;
  color: var(--font-color-1);
  background-color: var(--color-input-background-1);
  padding: 0 1rem;
  margin:.2rem ;
  font-size: 1.1rem;

  &::placeholder {
    text-align: center;
  }
}

.textarea-msg {
  display: block;
  font-family: var(--font-sans);
  border-radius: var(--border-radius);
  border: 1px solid var(--color-border-1);
  width: 100%;
  height: 8rem;
  color: var(--font-color-1);
  background-color: var(--color-input-background-1);
  padding: 1rem 1rem;
  margin: 0.2rem;
  font-size: .9rem;

}
.btn-send-form {
  margin: 20px 0;
  height: 60px;
  width: 36%;
  padding: 0 30px;
  background: none;
  font-weight: 700;
  font-size: 1rem;
  color: var(--color-wall-3);
  border: 2px solid var(--color-wall-3);
  border-radius: var(--border-radius);
  font-family: var(--font-mono);

  &:hover {
    background: var(--btn-hover-color);
  }

  @media screen and (max-width: 768px) {
    transition:0.2s;
    width: 40%;
  }

  @media screen and (max-width: 320px) {
    transition:0.2s;
    width: 56%;
  }
}
</style>
