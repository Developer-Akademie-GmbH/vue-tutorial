<template>
  <RecipeItem 
  :image="recipe.recipe.image"
  :label="recipe.recipe.label"
  :attributes="recipe.recipe.dietLabels.join(', ')"
  :url="recipe.recipe.url"
   v-for="recipe in recipes" />
</template>

<script>
import RecipeItem from '@/components/RecipeItem.vue';
export default {
  components: {
    RecipeItem
  },
  data() {
    return {
      recipes: []
    }
  },
  methods: {
    async getRecipes() {
      const query = 'curry';
      const appId = 'd7212edc';
      const appKey = '3515d1c2238911f0dde38cb661b1f67e';
      const url = `https://api.edamam.com/search?q=${query}&app_id=${appId}&app_key=${appKey}`;
      let resp = await fetch(url);
      this.recipes = (await resp.json()).hits;
      console.log(this.recipes);
    }
  },
  mounted(){
    this.getRecipes();
  }
}
</script>
