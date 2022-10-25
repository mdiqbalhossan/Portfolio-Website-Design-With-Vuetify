<template>
  <v-container class="pt-15">
    <v-row>
      <v-col lg="6">
        <h2 class="intro-text">Welcome to our Vuetify App</h2>
        <p class="description">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit.
          Exercitationem minima distinctio, asperiores neque reprehenderit
          voluptate excepturi dolor ea harum. Quidem laborum eaque odio vitae
          culpa quaerat, dignissimos officia in. Iusto?
        </p>
        <v-btn color="success" class="text-white mr-10" rounded
          >Get Started</v-btn
        >
        <v-btn color="indigo" rounded class="text-white">
          <v-icon>mdi-play-circle</v-icon> Watch Video
        </v-btn>
      </v-col>
      <v-col lg="6">
        <img width="100%" src="../assets/hero.jpg" alt="" />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {};
</script>

<style scoped>
h2.intro-text {
  font-size: 60px;
  font-weight: bold;
  font-family: cursive;
  color: #444;
}
p.description {
  font-size: 19px;
  font-family: cursive;
  margin: 32px 0px;
  color: #444444ba;
}
</style>