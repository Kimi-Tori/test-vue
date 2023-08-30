<template>
  <p class="form__subtitle">Закажите сейчас</p>
  <div class="form-conteiner">
    <form @submit.prevent="" class="form">
        <input class="form-input" type="text" id="name" v-model="formData.name" required placeholder="Ваше имя"/>
        <input class="form-input" type="tel" id="phone" v-model="formData.phone" required placeholder="Ваш телефон"/>
        <button class="form-button" type="submit">Отправить</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'FormComponent',
  data() {
    return {
      formData: {
        name: '',
        phone: '',
      },
    };
  },
};
</script>

<style scoped>
.form__subtitle {
    font-size: 28px;
    font-weight: 600;
    margin: 20px 0 10px 0;
    text-align: center;
}
.form-conteiner {
    display: flex;
    justify-content: center;
    margin-top: 20px;
}
.form {
    max-width: 600px;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px;
    background-color: #232c4b;
    border: 2px solid #0c1124;
    border-radius: 20px;
}
.form-input {
    width: calc(100% - 40px);
    margin-bottom: 10px;
    outline: none;
    border: 2px solid #0c1124;
    border-radius: 20px;
    padding: 10px 20px;
    font-size: 14px;
    text-align: center;
    color: #0c1124;
}
.form-input::placeholder {
    color: #0c1124;
}
.form-button {
    width: 100%;
    border-radius: 30px;
    outline: none;
    background-color: #fff;
    border: 2px solid #0c1124;
    padding: 10px 20px;
    cursor: pointer;
    font-size: 14px;
    font-weight: 600;
    letter-spacing: 2px;
    text-transform: uppercase;
    transition: 0.3s ease;
}
.form-button:hover {
    color: #fff;
    background-color: #0c1124;
    border: 2px solid #fff;
}
</style>