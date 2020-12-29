<template>

<div>
    <b-alert show> Этот компонент сверстан в странице {{pagename}} </b-alert>
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

}
</script>

<style lang=css>

    /* Стили для странички пишем тут */

</style>
