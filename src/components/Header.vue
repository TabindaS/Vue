<template>
    <header class="header">
        <div class="header__container">
            <div class="header__pauseButton"
                 @click="togglePause">
                <font-awesome-icon :icon="pauseButton"></font-awesome-icon>
            </div>
        </div>
    </header>
</template>

<script>
    import {faPlay, faPause} from '@fortawesome/free-solid-svg-icons'
    import {mapMutations, mapState} from 'vuex'
    import {TOGGLE_PAUSE} from '../constants'
    export default {
        name: 'Header',
        computed: {
            ...mapState({
                isPaused: state => state.isPaused
            }),
            pauseButton() {
                return this.isPaused ? faPlay : faPause
            }
        },
        methods: {
            ...mapMutations({
                togglePause: TOGGLE_PAUSE
            }),
        }
    }
</script>

<style scoped lang="scss">
    $primary-color: #1a1c2d;
    $secondary-color: #fff;
    .header {
        width: 100%;
        background-color: $primary-color;
        color: $secondary-color;
    }
    .header__container {
        display:flex;
        justify-content:center;
    }
    .header__pauseButton {
        width: 20%;
        cursor: pointer;
        font-size: 2rem;
        line-height: 2rem;
        padding: 1rem 0;
        display: flex;
        justify-content: center;
        align-items: center;
        transition: background-color 0.4s ease-in-out;
        &:hover {
            background-color: lighten($primary-color, 10%);
        }
    }
</style>