<template>
    <header>
        <nav>
            <ul>
                <li>
                    <nuxt-link to="/">Accueil</nuxt-link>
                </li>
                <li>
                    <nuxt-link to="recipes">Recettes</nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/about">A propos</nuxt-link>
                </li>
            </ul>
        </nav>
    </header>
</template>
<style scoped>
    header
    {
        width: 100%;
        height: 50px;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #521751;
    }

    ul
    {
        list-style: none;
        padding: 0;
        margin: 0;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    li 
    {
        margin: 0 10px;
    }

    a {
        color: white;
        text-decoration: none;
      }
</style>
