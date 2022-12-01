<template>
    <div>
        <div class="bg_img_left">
            <div class="signup_card_left" @click="goto('SignUpGlobiePage')">
                <div class="signup_card_outline">Globie</div>
            </div>
        </div>
        <div class="bg_img_right">
            <div class="signup_card_right" @click="goto('SignUpHostPage')">
                <div class="signup_card_outline">Host</div>
            </div>
        </div>
        <div class="page_container">
            <div class="sign_up_header">
                <div class="sign_up_header_outline">
                    What do you want to be
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data (){
        return {

        }
    },
    methods: {
        goto: function(to) {
            this.$router.push({name:to});
        }
    }
}
</script>

<style scoped>
    .signup_card_outline {
        border-style: solid;
        border-width: 3px;
        border-color: white;
        border-radius: 50%;
        width: 95%;
        height: 95%;
        display: flex;
        justify-content: center;
        align-items: center;
        transition: border-color 1s ease;
    }
    .signup_card_outline:hover {
        border-color: #c62034;
        transition: border-color 1s ease;
    }
    .signup_card_left {
        background-color: rgba(32, 40, 68, 1);
        width: 23vw;
        height: 23vw;
        border-radius: 50%;
        margin-left: 15%;
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        color: white;
        font-size: 2em;
        transition:color 1s ease, background-color 1s ease;
    }
    .signup_card_left:hover {
        color: #c62034;
        background-color: white;
        transition:color 1s ease, background-color 1s ease;
    }
    .signup_card_right {
        background-color: rgba(32, 40, 68, 1);
        width: 23vw;
        height: 23vw;
        border-radius: 50%;
        margin-right: 15%;
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        color: white;
        font-size: 2em;
        transition:color 1s ease, background-color 1s ease;
    }
    .signup_card_right:hover {
        color: #c62034;
        background-color: white;
        transition:color 1s ease, background-color 1s ease;
    }
    .sign_up_header_outline {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        font-size: 2.5rem;
        color: white;
        width: 98%;
        height: 85%;
        border-style: solid;
        border-radius: 1.5rem;
        border-color: white;
        border-width: 3px; 
    }
    .sign_up_header {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        font-size: 2.5rem;
        background-color: #c62034;
        color: white;
        width: 90%;
        height: 80%;
        border-radius: 2rem;
    }
    .page_container {
        display: flex;
        flex-direction: column;
        width: 100%;
        height: 10rem;
        justify-content: center;
        align-items: center;
    }
    .bg_img_left {
        background: linear-gradient( rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5) ), url("../assets/mountain.jpg");
        width: 100%;
        height: 100%;
        position: fixed;
        margin: 0;
        z-index: -2;
        background-position: center ;
        background-repeat: no-repeat;
        background-size: cover;
        clip-path: polygon(0 0, 60% 0, 40% 100%, 0 100%);
        transition: all 1s ease;
        display: flex;
        flex-direction: row;
        justify-content: flex-start;
        align-items: center;
    }
    .bg_img_left:hover {
        background: linear-gradient( rgba(0, 0, 0, 0), rgba(0, 0, 0, 0) ), url("../assets/mountain.jpg");
        width: 100%;
        height: 100%;
        position: fixed;
        margin: 0;
        z-index: -2;
        background-position: center ;
        background-repeat: no-repeat;
        background-size: cover;
        clip-path: polygon(0 0, 60% 0, 40% 100%, 0 100%);
        transition: all 1s ease;
    }
    .bg_img_right {
        background: linear-gradient( rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5) ), url("../assets/house.jpeg");
        width: 100%;
        height: 100%;
        position: fixed;
        margin: 0;
        z-index: -1;
        background-position: center ;
        background-repeat: no-repeat;
        background-size: cover;
        clip-path: polygon(60% 0, 100% 0, 100% 100%, 40% 100%);
        display: flex;
        flex-direction: row;
        justify-content: flex-end;
        align-items: center;
    }
    .bg_img_right:hover {
        background: linear-gradient( rgba(0, 0, 0, 0), rgba(0, 0, 0, 0) ), url("../assets/house.jpeg");
        width: 100%;
        height: 100%;
        position: fixed;
        margin: 0;
        z-index: -1;
        background-position: center ;
        background-repeat: no-repeat;
        background-size: cover;
        clip-path: polygon(60% 0, 100% 0, 100% 100%, 40% 100%);
    }
</style>