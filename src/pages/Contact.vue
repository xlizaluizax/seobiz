<template>
  <Layout>
    <div class="container">
      <div class="contact-header">
        <h1 class="contact-title">Девушка SEO-специалист и вебмастер?</h1>
        <p>Привет! Меня зовут Лиза, я "болею" SEO и интернет-маркетингом с 2013 года.
          <br>Надеюсь, Вам будет полезен мой опыт и эксперименты. Если у Вас возникнут какие-либо вопросы - смело пишите мне!
        </p>
      </div>

      <form class="contact-form" name="contact">
        <div class="sender-info">
          <div>
            <label for="name" class="label">Ваше имя</label>
            <input type="text" name="name">
          </div>
          <div>
            <label for="email" class="label">Ваш email</label>
            <input type="email" name="email">
          </div>
        </div>

        <div class="message">
          <label for="message" class="label">Сообщение</label>
          <textarea name="message"></textarea>
        </div>

        <button class="button">Отправить</button>
      </form>
    </div>
  </Layout>
</template>

<script>
export default {};
</script>

<style scoped>
.contact-header {
  padding: 2rem 0 4rem 0;
}
.contact-title {
  font-size: 4rem;
  margin: 0 0 4rem 0;
  padding: 0;
}
.sender-info {
  display: flex;
  flex-wrap: wrap;
  margin-bottom: 2rem;
}
.sender-info > div {
  flex: 1;
  margin-right: 4rem;
}
.sender-info > div:last-of-type {
  margin: 0;
}
input:focus,
textarea:focus {
  border-color: var(--color-contrast-1);
}
input,
textarea {
  background: transparent;
  border: 1px solid var(--color-base-1);
  outline: none;
  border-radius: 0.3rem;
  padding: 0.8rem 1rem;
  color: inherit;
  font-size: 1rem;
  width: 100%;
}
textarea {
  resize: none;
  height: 140px;
}
.button {
  color: var(--color-contrast-1);
  background: var(--color-base);
  outline: none;
  border: 1rem;
  border-color: var(--color-contrast-1);
  font-size: 1rem;
  padding: 0.8rem 1.6rem;
  border-radius: 2%;
  margin-top: 2rem;
  cursor: pointer;
  transition: opacity 0.25s ease;
  font-size: 500;
  letter-spacing: 0.035em;
}
.button:hover {
  opacity: 0.6;
}
.button:focus {
  border: 1px solid var(--color-contact-1);
}
</style>

