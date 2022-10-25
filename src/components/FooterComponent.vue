<template>
  <v-footer padless>
    <v-col lg="12">
      <v-row justify="center">
        <v-col lg="4" class="text-center">
          <v-toolbar-title>Web Application</v-toolbar-title>
          <v-card-text>
            <v-btn
              v-for="icon in icons"
              :key="icon"
              class="mx-4 black--text"
              icon
            >
              <v-icon size="24px">
                {{ icon }}
              </v-icon>
            </v-btn>
          </v-card-text>
          <v-subheader class="my-10"
            >Lorem, ipsum dolor sit amet consectetur adipisicing elit. Inventore
            commodi quaerat praesentium expedita, assumenda, sunt, tempora
            molestias dolor dolores accusantium illum facilis cupiditate
            mollitia! Facilis error qui odit quasi ex.</v-subheader
          >
          <v-form class="mt-4">
            <v-text-field label="E-mail" outlined dense></v-text-field>
            <v-btn rounded color="success">Subscribe Us</v-btn>
          </v-form>
        </v-col>
      </v-row>
      <div class="mt-10">
        <v-divider></v-divider>
        <v-subheader
          >©Copyright Web Application. All Right Reserved
          {{ new Date().getFullYear() }}

          <v-spacer></v-spacer>
          <strong>Designed By Md Iqbal</strong>
        </v-subheader>
      </div>
    </v-col>
  </v-footer>
</template>

<script>
export default {
  data() {
    return {
      icons: ["mdi-facebook", "mdi-twitter", "mdi-linkedin", "mdi-instagram"],
    };
  },
};
</script>

<style scoped>
.v-toolbar__title {
  font-size: 32px;
  color: #4caf50;
  font-weight: 700;
  font-family: cursive;
}
</style>