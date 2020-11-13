<template>
    <div class="index container">
        <div class="card" v-for="smoothie in smoothies" :key="smoothie.id">
            <div class="card-content">
                <h2 class="indigo-text">{{ smoothie.title }}</h2>

                <ul class="ingredients">
                    <li v-for="(ing, i) in smoothie.ingredients" :key="i">
                        <span class="chip">{{ ing }}</span>
                    </li>
                </ul>
            </div>

        </div>
    </div>
</template>

<script>
export default {
    name: 'Index',

    data() {
        return {
            smoothies: [
                {title: 'Recipe 1', slug: 'recipe 1', ingredients: ['Pineapple', 'Mangoes', 'Banana', 'Spinach'], id: '1'},
                {title: 'Recipe 2', slug: 'Recipe 2', ingredients: ['Pineapple', 'Mangoes', 'Banana', 'Celery'], id: '2'}
            ]
        }
    }
}
</script>

<style>
.index {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-gap: 30px;
    margin-top: 60px;
}

.index h2 {
    font-size: 1.8em;
    text-align: center;
    margin-top: 0;
}

.index .ingredients {
    margin: 30px auto;
}

.index .ingredients li {
    display: inline-block;
}
</style>