<template>
  <v-container class="my-15">
    <v-row justify-center>
      <v-col lg="12" class="text-center">
        <v-subheader class="text-h4 justify-center"> Contact Us </v-subheader>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Laudantium
          veritatis.
        </p>
      </v-col>
      <v-col lg="6">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d14639.913995436635!2d91.1833054!3d23.46124005!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1sen!2sbd!4v1666675928499!5m2!1sen!2sbd"
          width="100%"
          height="100%"
          style="border: 0"
          allowfullscreen=""
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
        ></iframe>
      </v-col>
      <v-col lg="6">
        <v-form ref="form">
          <v-text-field
            v-model="contactInfo.name"
            label="Name"
            required
          ></v-text-field>

          <v-text-field
            v-model="contactInfo.email"
            label="E-mail"
            required
          ></v-text-field>

          <v-textarea label="Message" v-moel="contactInfo.body"> </v-textarea>

          <v-btn color="success" class="mr-4"> Send </v-btn>
        </v-form>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      contactInfo: {
        name: null,
        email: null,
        body: null,
      },
    };
  },
};
</script>

<style scoped>
</style>