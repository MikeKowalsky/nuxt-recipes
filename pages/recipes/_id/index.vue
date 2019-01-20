<template>
  <section class="single-recipe">
    <h1>{{ recipe.title }}</h1>
    <div>
      <img class="recipe-image" :src="recipe.thumbnail" :alt="recipe.title">
    </div>
    <p>{{ recipe.descriptionText }}</p>
  </section>
</template>

<script>
export default {
  //context it's a nuxt tool we can use to retreive id from url -> in .find we cannot use $route because asyncData happens beforme component is build, so does not exist
  asyncData(context) {
    //fake api call
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipe: [
            {
              id: "1",
              title: "China Nudle",
              previewText: "Glassnudle with vegetables!",
              descriptionText:
                "This is really delicious meal! You need to eat this!",
              thumbnail:
                "https://ichef.bbci.co.uk/food/ic/food_16x9_832/recipes/one_pot_chorizo_and_15611_16x9.jpg"
            },
            {
              id: "2",
              title: "Seitan Spaghetti",
              previewText: "Almost like meet one ;-)",
              descriptionText:
                "This is really delicious meal! You need to eat this!",
              thumbnail:
                "https://static.independent.co.uk/s3fs-public/thumbnails/image/2017/02/07/15/chinese.jpg?w968h681"
            }
          ].find(el => el.id === context.params.id)
        });
      }, 1500);
    });
  }
};
</script>


<style scoped>
.single-recipe {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 30px;
}

.recipe-image {
  width: 80%;
}
</style>

