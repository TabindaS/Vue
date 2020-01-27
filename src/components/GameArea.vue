<template>
    <main class="gameArea">
        <Dropbox/>
        <TeeterTotter/>
    </main>
</template>

<script>
    import Dropbox from './Dropbox'
    import TeeterTotter from './TeeterTotter'
    export default {
        name: "GameArea",
        components:{
            Dropbox, TeeterTotter
        }
    }
</script>

<style lang="scss" scoped>
    .gameArea {
        width: 80%;
        height: 100%;
        margin: 0 auto;
        display: flex;
        flex-direction: column;
        padding-top: 1rem;
    }
</style>