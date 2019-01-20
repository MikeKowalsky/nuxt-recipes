<template>
  <section class="recipes">
    <Recipe 
      thumbnail="https://ichef.bbci.co.uk/food/ic/food_16x9_832/recipes/one_pot_chorizo_and_15611_16x9.jpg"
      title="China Nudle"
      id="1"
      previewText="Glassnudle with vegetables!"
    />
    <Recipe 
      thumbnail="https://static.independent.co.uk/s3fs-public/thumbnails/image/2017/02/07/15/chinese.jpg?w968h681"
      title="Seitan Spaghetti"
      id="2"
      previewText="Almost like meet one ;-)"
    />
  </section>
</template>

<script>
import Recipe from "@/components/Recipe";
export default {
  components: {
    Recipe
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
