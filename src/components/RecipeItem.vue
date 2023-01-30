<template>
    <a :href="url" class="recipeItemContainer">
        <img class="recipe-image" :src="image" />
        <div class="right-side">
            <div>
                {{ label }}
            </div>
            <div class="bottom-row">
                {{ attributes }}
            </div>
        </div>
    </a>
</template>


<script>
export default {
    name: 'RecipeItem',
    props: {
        image: String,
        label: String,
        attributes: String,
        url: String
    }
}
</script>

<style scoped>
.recipeItemContainer {
    border: 1px solid rgba(0, 0, 0, 0.2);
    padding: 8px;
    border-radius: 8px;
    margin: 8px;
    display: flex;
    gap: 8px;
    cursor: pointer;
    text-decoration: none;
    color: rgba(0, 0, 0, 0.8);
}

.recipeItemContainer:hover {
    background-color: rgba(0, 0, 0, 0.05);
}

.recipe-image {
    height: 60px;
    border-radius: 8px;
}

.right-side {
    display: flex;
    flex-direction: column;
    /* justify-content: space-between; */
}

.bottom-row {
    color: rgba(0, 0, 0, 0.4);
    font-size: 12px;
}
</style>