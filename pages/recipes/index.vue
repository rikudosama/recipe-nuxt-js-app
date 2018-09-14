<template>
    <section class="recipes">
        <article class="recipe">
            <div class="thumbnail" style="background-image: url('../../assets/img/pizza.jpg');"></div>
            <h1>Le titre de la nourriture</h1>
            <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
            </p>
        </article>
        <article class="recipe">
            <div class="thumbnail" style="background-image: url('/assets/img/humberger.jpg');"></div>
            <h1>Le titre de la nourriture</h1>
            <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
            </p>
        </article>
        <article class="recipe">
            <div class="thumbnail" style="background-image: url('/assets/img/salade.jpg');"></div>
            <h1>Le titre de la nourriture</h1>
            <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
            </p>
        </article>
    </section>
</template>
<style scoped>
    .recipes
    {
        display: flex;
        flex-flow: row wrap;
        justify-content: center;
        align-content: center;
    }

    .recipe
    {
        box-sizing: border-box;
        width: 280px;
        padding: 8px;
        border: 1px solid #ccc;
        box-shadow: 0 2px 2px #aaa;
        margin: 10px;
    }

    .thumbnail 
    {
        background-position: center;
        background-size: cover;
        width: 100%;
        height: 200px;
    }
</style>
