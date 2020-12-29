<template>

<div>
    <b-alert show> Этот компонент сверстан в странице {{pagename}} </b-alert>

    <b-button v-on:click="loadData()">Button</b-button>

</div>

</template>

<script>
export default {

    layout: 'default',

    data() {
        return {
            pagename: "Главная",
        }
    },

    // тестовый запрос для демонстрации возможностей

    async asyncData({ $axios }) {

        let planet = await $axios.$get('https://swapi.dev/api/planets/1');
        console.log(planet)
        return { planet }

    },

    methods: {
        loadData: function () {
            this.$axios.$get('https://swapi.dev/api/planets/2').then((result) => {
                console.log(result)
                }
            )

        }
    }

}
</script>

<style lang=css>

    /* Стили для странички пишем тут */

</style>
