<template>

  <v-form class="contact" my-5 action="https://formspree.io/skorupapiotr1@gmail.com" method="post">
    <h1>Contact</h1>
    <h2>In order to get in touch with me, use the form below<br>or e-mail me directly: skorupapiotr1@gmail.com</h2>

    <v-text-field v-model="name" label="Name" required></v-text-field>
    <v-text-field v-model="email" label="E-mail" required></v-text-field>
    <v-textarea v-model="message" label="Message"></v-textarea>
    <v-btn color="success" type="submit">
      Submit
    </v-btn>
  </v-form>
</template>
<script>
export default {
  name: "Contact",
  data:() => ({
    name: 'Name',
    email: 'E-Mail',
    message: 'Message'
  })
};
</script>

<style>
.contact {
  max-width: 1000px;
  margin: auto;
  margin-top: 5rem;
}
</style>

