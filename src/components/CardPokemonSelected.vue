<script setup>

const pokemon = defineProps(["name", "xp", "height", "img", "loading"])

</script>
<template>
    <div class="card CardPokemonSelected " :class="loading ? '' : 'animate__animated animate__fadeInDown'">
        <img v-if="pokemon.name" :src="pokemon.img" class="card-img-top pt-2" :alt="pokemon.name" />
        <img v-else src="../assets/egg_pokemon.svg" class="card-img-top pt-2" alt="????" />
        <div class="card-body text-black ">
            <h5 class=" card-title text-center"><strong>{{ pokemon.name || '???' }}</strong></h5>
            <hr>
            <div class="infor row ">
                <section class="col ">
                    <strong>XP: </strong>
                    <span><strong>{{ pokemon.xp }}</strong></span>
                </section>
                <section class="col ">
                    <strong>Altura: </strong>
                    <span><strong>{{ pokemon.height }} cm</strong></span>
                </section>
            </div>
        </div>
    </div>

</template>


<style scoped>
.CardPokemonSelected {
    height: 75vh;
    background: rgb(191, 0, 255);
    background: radial-gradient(circle, rgb(191, 0, 255) 0%, rgba(19, 18, 70, 1) 75%);
}

.CardPokemonSelected img {
    height: 300px;
}

@media (max-width: 600px) {
    .CardPokemonSelected {
        height: 35vh;
        width: 70%;
        margin: 0 auto 10px auto;
        
    }

    .CardPokemonSelected img {
        height: 155px;
    }
    .CardPokemonSelected .infor{
        padding: 0 0 0 5%;
        
    }

}

h5::first-letter {
    text-transform: uppercase;
}

.infor {
    padding-left: 20%
}
</style>