<template>
  <section class="recipes">
    <Recipe
      v-for="rec in recipes"
      :key="rec.id"
      :thumbnail="rec.thumbnail"
      :title="rec.title"
      :id="rec.id"
      :previewText="rec.previewText"
    />
  </section>
</template>

<script>
import Recipe from "@/components/Recipe";
export default {
  components: {
    Recipe
  },
  // this async data will be merge with normal data then template will be created, it means that the server will "fetch data" render component and then will send it to the user
  asyncData() {
    //fake api call
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipes: [
            {
              id: "1",
              title: "China Nudle",
              previewText: "Glassnudle with vegetables!",
              thumbnail:
                "https://ichef.bbci.co.uk/food/ic/food_16x9_832/recipes/one_pot_chorizo_and_15611_16x9.jpg"
            },
            {
              id: "2",
              title: "Seitan Spaghetti",
              previewText: "Almost like meet one ;-)",
              thumbnail:
                "https://static.independent.co.uk/s3fs-public/thumbnails/image/2017/02/07/15/chinese.jpg?w968h681"
            }
          ]
        });
      }, 1500);
    });
  }
};
</script>


<style scoped>
.recipes {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items: center;
}
</style>
