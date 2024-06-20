<script setup>
const pokemon = defineProps(["name", "urlBaseSvg"])

</script>

<template>
    <div class="col-4 col-md-6 col-lg-3">
        <div class="card p-2 mb-3 cardListPokemon text-black " >
            <p class="text-center "><strong>{{ pokemon.name }}</strong></p>
            <img :src="pokemon.urlBaseSvg" class="card-img-top" alt="" height="80" />
        </div>
    </div>
</template>

<style scoped>
.cardListPokemon {
    background-color: rgb(0, 42, 255);
    background-color: radial-gradient(circle, rgba(0, 42, 255, 1) 0%, rgba(19, 18, 70, 1) 75%);
    cursor: pointer;
}

.cardListPokemon:hover {
    background-color: rgb(25, 55, 208);
    background-color: radial-gradient(circle, rgba(25, 55, 208, 1) 0%, rgba(17, 17, 56, 1) 75%);
}
.cardListPokemon img:hover {
    padding: .1rem;
}
p::first-letter{
    text-transform: uppercase;
}
</style>