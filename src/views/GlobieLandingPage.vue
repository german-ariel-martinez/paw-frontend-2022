<template>
    <div class="postsDisplay">
        <!-- Panel de filtros -->
        <div class="filterMenu">
            <ul class="filters">
                <li></li>
                <li></li>
                <li></li>
            </ul>
        </div>
        <!-- Posts -->
        <div class="postsViewer">
            h
        </div>
    </div>
</template>

<style scoped>
    .postsDisplay {
        display: grid;
        height: 100%;
        justify-items: center;
        align-items: center;
        grid-template-columns: 1.125fr 4fr;
    }
    .filterMenu {
        display: grid;
        height: 100%;
        width: 100%;
        background-color: purple;
    }
    .postsViewer {
        display: grid;
        width: 100%;
        height: 100%;
        background-color: greenyellow;
    }
</style>

<script>
export default {
    name: 'HomePage',
    methods: {
        sotm(){
            this.$router.push('/home/sotm')
        }
    }
}
</script>