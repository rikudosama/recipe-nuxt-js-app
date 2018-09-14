<template>
    <section class="recipes">
        <recipe 
        thumbnail="assets/img/pizza.jpg"
        title="Savoureuse pizza"
        previewDescription=" Lorem ipsum dolor sit amet consectetur adipisicing elit."
         />

         <recipe 
         thumbnail="assets/img/humberger.jpg"
         title="Un big belly burger"
         previewDescription=" Lorem ipsum dolor sit amet consectetur adipisicing elit."
         />

        <recipe 
         thumbnail="assets/img/salade.jpg"
         title="Une salade 100% bio"
         previewDescription=" Lorem ipsum dolor sit amet consectetur adipisicing elit."
         />
        
    </section>
</template>
<script>
import Recipe from '~/components/Recipe';
export default {
    components: {
        Recipe
    }
}
</script>

<style scoped>
    .recipes
    {
        display: flex;
        flex-flow: row wrap;
        justify-content: center;
        align-content: center;
    }
</style>
