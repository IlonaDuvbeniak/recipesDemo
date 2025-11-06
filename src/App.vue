<script>
    import Card from './components/Card.vue'

    export default {
        components: {
            Card
        },
        data() {
            return {
                coctails: [
                    { id: 0, categori: 'Post-Breakup Potions', name: 'Bye Bye Mary', image: '/img/drinks/bloody-mary.png', rating: 4.6, ingridients: 5, time: 15},
                    { id: 1, categori: 'Drunk in paradise', name: 'Out of office', image: '/img/drinks/out-of-office.png', rating: 4.9, ingridients: 4, time: 10},
                    { id: 2, categori: 'Party Like It’s Friday', name: 'Dancing on Tables', image: '/img/drinks/dancing-on-tables.png',rating: 4.8, ingridients: 6, time: 8},
                    { id: 3, categori: 'Boos & Brews', name: 'Witch, Please!',image: '/img/drinks/witch-please.png', rating: 4.8, ingridients: 5, time: 7},
                    { id: 4, categori: 'Sips of Christmas', name: 'Mistle-Toasted', image: '/img/drinks/mistle-toast.png',rating: 4.5, ingridients: 6, time: 9},
                    { id: 5, categori: 'Post-Breakup Potions', name: 'Exorcism', image: '/img/drinks/exorcism.png', rating: 5, ingridients: 3, time: 12}
                ]   
            }
        }
    }
    

</script>

<template>
    <div class="cards-container">
        <Card
            v-for="coctail in coctails"
            :key="coctail.id"
            :categori="coctail.categori"
            :name="coctail.name"
            :rating="coctail.rating"
            :ingridients="coctail.ingridients"
            :time="coctail.time"
            :image="coctail.image"
            :label="coctail.name"
        />
    </div>
</template>

<style scoped>
    .cards-container {
        display: grid;
        grid-template-columns: auto auto auto;
        width: 100%;
        gap: 24px;
    }
</style>
