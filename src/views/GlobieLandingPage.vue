<template>
    <div class="postsDisplay">
        <!-- Panel de filtros -->
        <div class="filterMenu">
            <div class="filter_section_title">
                <span class="title">Here you can filter posts</span>
            </div> 
            <ul class="buttons">
                <li><v-select label="Order by" outlined></v-select></li>
                <li><v-select label="Show ratings" outlined></v-select></li>
                <li><v-select label="Select country" outlined></v-select></li>
            </ul>
            <!-- Lenguajes checkboxes -->
            <div class="filter_section_title">
                <span class="title">Languages</span>
            </div>
            <div class="languages">
                <ul class="checkboxes" style="margin-left: 10%">
                    <li><v-checkbox v-model="checkbox" label="Spanish"></v-checkbox></li>
                    <li><v-checkbox v-model="checkbox" label="German"></v-checkbox></li>
                    <li><v-checkbox v-model="checkbox" label="Italian"></v-checkbox></li>
                </ul>
                <ul class="checkboxes">
                    <li><v-checkbox v-model="checkbox" label="Japanese"></v-checkbox></li>
                    <li><v-checkbox v-model="checkbox" label="Korean"></v-checkbox></li>
                    <li><v-checkbox v-model="checkbox" label="Portuguese"></v-checkbox></li>
                </ul>
            </div>
            <!-- Caracteristicas de los departamentes -->
            <div class="filter_section_title">
                <span class="title">Post features</span>
            </div>
            <div class="languages">
                <ul class="checkboxes" style="margin-left: 10%">
                    <li><v-checkbox v-model="checkbox" label="Pool"></v-checkbox></li>
                    <li><v-checkbox v-model="checkbox" label="Allow pets"></v-checkbox></li>
                    <li><v-checkbox v-model="checkbox" label="Gym"></v-checkbox></li>
                </ul>
                <ul class="checkboxes">
                    <li><v-checkbox v-model="checkbox" label="Yard"></v-checkbox></li>
                    <li><v-checkbox v-model="checkbox" label="TV"></v-checkbox></li>
                    <li><v-checkbox v-model="checkbox" label="Wifi"></v-checkbox></li>
                </ul>
            </div>       
        </div>
        <!-- Posts -->
        <div class="postsViewer">
            <card location="Australia, Victoria" languages="French, German, Portuguese, Dutch" rating="5"/>
            <card location="Australia, Victoria" languages="French, German, Portuguese, Dutch" rating="5"/>
            <card location="Australia, Victoria" languages="French, German, Portuguese, Dutch" rating="5"/>
            <card location="Australia, Victoria" languages="French, German, Portuguese, Dutch" rating="5"/>
            <card location="Australia, Victoria" languages="French, German, Portuguese, Dutch" rating="5"/>
            <card location="Australia, Victoria" languages="French, German, Portuguese, Dutch" rating="5"/>
            <card location="Australia, Victoria" languages="French, German, Portuguese, Dutch" rating="5"/>
            <card location="Australia, Victoria" languages="French, German, Portuguese, Dutch" rating="5"/>
            <card location="Australia, Victoria" languages="French, German, Portuguese, Dutch" rating="5"/>
            <card location="Australia, Victoria" languages="French, German, Portuguese, Dutch" rating="5"/>
        </div>
    </div>
</template>

<style scoped>
    .postsViewer {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        align-items: center;
        justify-items: center;
        width: 100%;
        height: 100%;
        background-color: rgba(39,42,53,0.3);
        overflow-y: auto;
    }
    .languages {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
    }
    .checkboxes {
        list-style-type: none;
        display: flex;
        flex-direction: column;
        width: 90%;
        justify-content: flex-start;
        align-items: flex-start;
        margin:0;
        padding: 0;
    }
    .checkboxes li {
        list-style-type: none;
        display: flex;
        flex-direction: row;
        justify-content: flex-start;
        align-items: center;
        margin:0;
        padding: 0;
    }
    .title {
        border-top-style: solid;
        border-bottom-style: solid;
        border-width: .15vh;
        border-color:white;
        height: 90%;
        width: 100%;
        margin: 0;
        padding: 0;
        font-size: 2vh;
    }
    .filter_section_title {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        background-color: #202844;
        color: white;
        height: 4vh;
        margin: 0;
        padding: 0;
    }
    .buttons {
        width: 100%;
        margin-top: 2.5vh;
    }
    .buttons li {
        list-style-type: none;
        display: flex;
        flex-direction: row;
        height: 10vh;
        width: 90%;
        justify-content: center;
        align-items: center;
        margin:0;
        padding: 0;
    }
    .buttons li:first-child {
        margin-top:6vh;
    }
    .postsDisplay {
        display: grid;
        height: 100%;
        justify-items: center;
        align-items: center;
        grid-template-columns: 1.125fr 4fr;
    }
    .filterMenu {
        height: 100%;
        width: 100%;
        margin:0;
        padding: 0;
        overflow-y: auto;
    }
    .filterMenu::-webkit-scrollbar{
        display: none;
    }
</style>

<script>
import card from '@/components/postCard.vue'
export default {
    components: {
        card,
    }
}
</script>