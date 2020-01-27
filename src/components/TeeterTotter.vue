<template>
    <section class="teeterTotter">
        <Swing/>
        <Pillar/>
    </section>
</template>

<script>
    import Swing from './Swing'
    import Pillar from './Pillar'
    export default {
        name: "TeeterTotter",
        components: {
            Swing, Pillar
        }
    }
</script>

<style scoped>
    .teeterTotter{
        height: 35%;
        width: 100%;
    }
</style>