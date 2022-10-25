<template>
  <v-container class="my-15">
    <v-row justify="center">
      <v-col lg="12" class="text-center">
        <v-subheader class="text-h4 justify-center">Portfolio</v-subheader>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam
          consequatur.
        </p>
      </v-col>
      <v-col lg="12">
        <div class="text-center">
          <v-chip
            @click="activePortfolio = 'webDesign'"
            :color="activePortfolio == 'webDesign' ? 'success' : ''"
            class="mx-5"
            >Web Design</v-chip
          >
          <v-chip
            @click="activePortfolio = 'webDevelopment'"
            :color="activePortfolio == 'webDevelopment' ? 'success' : ''"
            class="mx-5"
            >Web Development</v-chip
          >
          <v-chip
            @click="activePortfolio = 'appDevelopment'"
            :color="activePortfolio == 'appDevelopment' ? 'success' : ''"
            class="mx-5"
            >App Development</v-chip
          >
        </div>
      </v-col>
      <slot v-if="activePortfolio == 'webDesign'">
        <v-col lg="3" v-for="(wd, wdindex) in webDesign" :key="wdindex">
          <v-card>
            <v-img
              :src="wd.image"
              class="white--text align-end"
              gradient="to bottom, rgba(0,0,0,.1),rgba(0,0,0,0.5)"
              height="200px"
            >
              <v-card-title v-text="wd.title"></v-card-title>
            </v-img>
          </v-card>
        </v-col>
      </slot>
      <slot v-if="activePortfolio == 'webDevelopment'">
        <v-col lg="3" v-for="(wd, wdindex) in webDevelopment" :key="wdindex">
          <v-card>
            <v-img
              :src="wd.image"
              class="white--text align-end"
              gradient="to bottom, rgba(0,0,0,.1),rgba(0,0,0,0.5)"
              height="200px"
            >
              <v-card-title v-text="wd.title"></v-card-title>
            </v-img>
          </v-card>
        </v-col>
      </slot>
      <slot v-if="activePortfolio == 'appDevelopment'">
        <v-col lg="3" v-for="(ad, adindex) in appDevelopment" :key="adindex">
          <v-card>
            <v-img
              :src="ad.image"
              class="white--text align-end"
              gradient="to bottom, rgba(0,0,0,.1),rgba(0,0,0,0.5)"
              height="200px"
            >
              <v-card-title v-text="ad.title"></v-card-title>
            </v-img>
          </v-card>
        </v-col>
      </slot>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      activePortfolio: "webDesign",
      webDesign: [
        {
          title: "Web Design 1",
          image:
            "https://static.vecteezy.com/system/resources/thumbnails/005/879/568/small/web-designer-modern-flat-concept-for-web-banner-design-man-working-with-website-layout-places-images-and-other-graphic-elements-optimized-page-code-illustration-with-isolated-people-scene-vector.jpg",
        },
        {
          title: "Web Design 2",
          image:
            "data:image/png;base64,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",
        },
        {
          title: "Web Design 3",
          image:
            "https://img.freepik.com/free-vector/web-development-programmer-engineering-coding-website-augmented-reality-interface-screens-developer-project-engineer-programming-software-application-design-cartoon-illustration_107791-3863.jpg",
        },
        {
          title: "Web Design 4",
          image:
            "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSa8Gs2JeMSq5K0Bc_Ndj0zMbE19MjMUgX_-33CKq6CfDTc-Gz8bCbK9dT2-mp7EV_SN4I&usqp=CAU",
        },
      ],
      webDevelopment: [
        {
          title: "Web Development 1",
          image:
            "https://static.vecteezy.com/system/resources/thumbnails/005/879/568/small/web-designer-modern-flat-concept-for-web-banner-design-man-working-with-website-layout-places-images-and-other-graphic-elements-optimized-page-code-illustration-with-isolated-people-scene-vector.jpg",
        },
        {
          title: "Web Development 2",
          image:
            "https://99designs-blog.imgix.net/blog/wp-content/uploads/2018/09/WHAT-IS-WEB-DESIGN.jpg?auto=format&q=60&w=1860&h=1046.25&fit=crop&crop=faces",
        },
        {
          title: "Web Development 3",
          image:
            "https://usabilitygeek.com/wp-content/uploads/2019/02/psychology-web-design-00-lead.jpg",
        },
        {
          title: "Web Development 4",
          image:
            "https://images.ctfassets.net/gg4ddi543f5b/7AHjFKPTt6B5ZwI8oI52rN/862db70ca26d7a72ce642932527e252d/web-design-workflow-blog.png",
        },
      ],
      appDevelopment: [
        {
          title: "App Development 1",
          image:
            "https://somosalameda.org/wp-content/uploads/2021/01/App-Development-4.jpg",
        },
        {
          title: "App Development 2",
          image: "https://tateeda.com/wp-content/uploads/2020/10/1-14.jpg",
        },
        {
          title: "App Development 3",
          image:
            "https://media.designrush.com/articles/101246/conversions/app-development-process-preview.jpg",
        },
        {
          title: "App Development 4",
          image:
            "https://appedus.com/wp-content/uploads/2021/09/app-development-1.png",
        },
      ],
    };
  },
};
</script>

<style scoped>
</style>