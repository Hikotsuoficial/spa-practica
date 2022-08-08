<template>
  <h1>Hacemos un proyecto?</h1>
  <div class="form-container">
    <h5 class="description__title2">Contáctame</h5>
    <form action="https://formspree.io/f/mgedqodg" method="POST">
      <ul class="order-form">
        <li>
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
        </li>
        <li>
          <label class="label" for="mail"
            >Correo electrónico
            <input class="contact-input" type="email" name="email" required />
          </label>
        </li>
        <li>
          <label class="label" for="message"
            >Mensaje
            <textarea
              class="textareaMsg"
              minlength="20"
              maxlength="400"
              name="message"
              placeholder="Escribe tu mensaje aquí"
              rows="4"
              required
            ></textarea>
          </label>
        </li>
        <li><button type="submit">Enviar</button></li>
      </ul>
    </form>
  </div>
</template>

<style lang="scss" scoped>
@import '@/assets/styles/main.scss';

.order-form{
    list-style: none;
}
.label{
    margin: 2rem;
}
.contact-input{
    display: block;
    border-radius: var(--border-radius);
    border: 1px solid var(--color-border-1);
    width: 25%;
    height: 3.5rem;
    color: var(--font-color-1);
    background-color: var(--color-wall-4);
    padding: 0 1rem;
    margin: 1rem;
    font-size: 1.2rem;

    &::placeholder{
        text-align: center;
    }
}
</style>
