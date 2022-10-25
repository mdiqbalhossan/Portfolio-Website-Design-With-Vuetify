<template>
  <v-app>
    <app-bar></app-bar>
    <v-main>
      <hero-section></hero-section>
      <about-us></about-us>
      <portfolio-component></portfolio-component>
      <project-component></project-component>
      <gallery-component></gallery-component>
      <contact-us></contact-us>
      <footer-component></footer-component>
    </v-main>
  </v-app>
</template>

<script>
import AppBar from "./components/AppBar";
import HeroSection from "./components/HeroSection";
import AboutUs from "./components/AboutUs";
import PortfolioComponent from "./components/PortfolioComponent";
import ProjectComponent from "./components/ProjectComponent";
import GalleryComponent from "./components/GalleryComponent";
import ContactUs from "./components/ContactUs";
import FooterComponent from "./components/FooterComponent";
export default {
  name: "App",
  components: {
    AppBar,
    HeroSection,
    AboutUs,
    PortfolioComponent,
    ProjectComponent,
    GalleryComponent,
    ContactUs,
    FooterComponent,
  },
};
</script>
