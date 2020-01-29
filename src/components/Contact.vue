<template>
  <section id="contact">
    <h2>Entre em contato</h2>
    <p>Entre em contato e peça um orçamento ou tire uma duvida! :)</p>
    <form @submit.prevent="sendEmail" class="contact-form container">
      <div class="input-form">
        <input type="text" placeholder="Seu nome" v-model="name"/>
        <input type="email" placeholder="Seu e-mail" v-model="email"/>
        <input type="tel" placeholder="Seu telefone" v-model="phone"/>
        <input type="text" placeholder="Assunto" v-model="subject"/>
      </div>
      <textarea placeholder="Digite aqui..." v-model="message"/>
      <button type="submit"><img :src="Enter" alt="enviar"></button>

      <label class="nao-aparece">Se você não é um robô, deixe em branco.</label>
      <input type="text" class="nao-aparece" name="leaveblank" />
      <label class="nao-aparece">Se você não é um robô, não mude este campo.</label>
      <input type="text" class="nao-aparece" name="dontchange" value="http://" />

    </form>
  </section>
</template>

<script>
import Enter from '../assets/icons/Enter.png'
import emailjs from 'emailjs-com';
import Swal from 'sweetalert2';
import 'sweetalert2/src/sweetalert2.scss'

export default {
  name: "Contact",
  data: () => ({
    Enter,
    name: '',
    email: '',
    phone: '',
    subject: '',
    message: '',
  }),
  methods: {
    sendEmail() {
      const templateParams = {
        name: this.name,
        email: this.email,
        phone: this.phone,
        subject: this.subject,
        message: this.subject,
      };
      emailjs.send('gmail', 'template_YGm7YMlb', templateParams, 'user_yrAnNFe9nyioAbKbOmHYH')
        .then(response => {
          Swal.fire({
            title: 'Sucesso',
            icon: 'success',
            confirmButtonText: response.text
          })
        }, error => {
          Swal.fire({
            title: 'Erro!',
            icon: 'error',
            confirmButtonText: error
          })
        });
    }
  },
};
</script>

<style lang="scss" scoped>
section {
  background-image: url("../assets/images/concert.png");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: fixed;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 50px;
  padding-bottom: 150px;
  & h2 {
    text-align: center;
    color: $light;
    padding: 50px 0 20px;
    font-size: 2em;
    text-shadow: 0px 1px 3px $dark;
  }
  & p {
    font-style: italic;
    color: $light;
    font-weight: 300;
    text-align: center;
    padding: 0 0 50px;
  }
  & form {
    display: flex;
    & .input-form {
      display: flex;
      flex-direction: column;
      & input {
        flex: 1;
        min-width: 300px;
        margin: 10px;
        border: none;
        border-radius: 10px;
        padding: 10px 20px;
        font-size: 1.2em;
        background: $light;
        font-weight: 500;
        box-shadow: 0 0 2px 1px rgba($color: $dark, $alpha: 0.12);
      }
    }
    & textarea {
      flex: 1;
      min-width: 300px;
      min-height: 200px;
      margin: 10px;
      border: none;
      border-radius: 10px;
      padding: 10px 20px;
      font-size: 1.2em;
      background: $light;
      font-weight: 500;
      box-shadow: 0 0 2px 1px rgba($color: $dark, $alpha: 0.12);
    }
    & button {
      flex: 1;
      display: flex;
      justify-content: center;
      align-items: center;
      margin: 10px;
      background: $primary;
      border: none;
      border-radius: 10px;
      padding: 5px;
      cursor: pointer;
      box-shadow: 0 0 2px 1px rgba($color: $dark, $alpha: 0.12);
      transition: all 0.3s;
      &:hover {
        background: $secondary;
      }
    }
  }
  & .nao-aparece {
    display: none;
  }
}
@media screen and (max-width: 762px) {
  section {
    flex-direction: column;
    align-items: center;
    padding-top: 0px;
    padding-bottom: 50px;
    & p {
      font-style: italic;
      color: $light;
      font-weight: 300;
      text-align: center;
      padding: 0 20px 20px;
    }
    & form {
      display: flex;
      flex-direction: column;
      padding: 0 20px 20px;
    }
    & button {
      & img {
        &::before {
          content: ' Enviar'
        }
      }
    }
  }
}
</style>