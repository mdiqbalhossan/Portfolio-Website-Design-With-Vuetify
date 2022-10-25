<template>
  <v-container class="my-15">
    <v-row justify-center>
      <v-col lg="12" class="text-center">
        <v-subheader class="text-h4 justify-center"> Project </v-subheader>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Laudantium
          veritatis.
        </p>
      </v-col>
      <v-col lg="4" v-for="project in 3" :key="project">
        <v-card class="mx-auto my-12" max-width="374">
          <v-img height="250" src="../assets/portfolio/1.jpg"> </v-img>
          <v-card-title>Web Development</v-card-title>
          <v-card-text>
            <div>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita
              necessitatibus Placeat, eligendi tempora.
            </div>
          </v-card-text>
          <v-divider class="mx-4"></v-divider>
          <v-card-action>
            <v-btn color="success" class="my-3 mx-3" rounded
              >View Details</v-btn
            >
          </v-card-action>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {};
</script>

<style scoped>
</style>