<template>
    <div>
        <div class="layer_one"></div>
        <div class="layer_two"></div>
        <div class="layer_three"><span class="asd">Hi Globie, welcome to the family!</span></div>
        <div class="background">
            <div class="nav">
                <div class="icon_outline" @click="goto('LandingPage')">
                    <b-icon icon="arrow-left" class="return_home_icon"></b-icon>
                </div> 
            </div>
            <div class="form_container">
                <div class="form_card">
                    <div class="form_card_main_column">
                        <div class="form_title">
                            Register
                        </div>
                        <div class="form_form">
                            <form class="form_main_col" action="">
                                <div class="form_row">
                                    <input class="form_input" type="text" id="fname" name="firstname" placeholder="Enter your email">
                                </div>
                                <div class="form_row_2">
                                    <div class="form_col" style="margin-right:5%;">
                                        <input class="form_input" type="text" id="fname" name="firstname" placeholder="Enter your password">
                                    </div>
                                    <div class="form_col">
                                        <input class="form_input" type="text" id="fname" name="firstname" placeholder="Confirm password">
                                    </div>
                                </div>
                                <div class="form_row_2">
                                    <div class="form_col" style="margin-right:5%;">
                                        <input class="form_input" type="text" id="fname" name="firstname" placeholder="Enter your name">
                                    </div>
                                    <div class="form_col">
                                        <input class="form_input" type="text" id="fname" name="firstname" placeholder="Enter your lastname">
                                    </div>
                                </div>
                                <div class="form_row_3">
                                    <textarea class="form_textarea" name="textarea" placeholder="Describe your goals here..."></textarea>
                                </div>
                            </form>
                        </div>
                    </div>
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
.asd {
    margin-right:1vw;
    margin-top:1.5vh;
    color:black;
}
.nav_title {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-self: flex-end;
}
.form_textarea {
    width: 100%;
    height: 100%;
    margin-top: 4vh;
    margin-bottom: 1vh;
    border-radius: 1em;
    border-style: solid;
    border-width: .5px;
    border-color: rgba(0, 0, 0, 0.4);
    padding-left: 1vw;
    padding-right: 1vw;
    padding-top: .5vw;
}
.form_row_3 {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    height: 100%;
}
.form_row_2 {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
}
.form_col {
    display: flex;
    flex-direction: column;
    width: 50%;
}
.form_row {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
}
.form_input {
    margin-top: 2vh;
    border-radius: 2em;
    border-style: solid;
    border-width: .5px;
    border-color: rgba(0, 0, 0, 0.4);
    padding-left: 1vw;
    height: 5vh;
    width: 100%;
}
.form_main_col {
    display: flex;
    flex-direction: column;
    width: 90%;
}
.form_form {
    display: flex;
    flex-direction: row;
    justify-content: center;
    height: 80%;
}
.form_title {
    display: flex;
    flex-direction: row;
    align-items: center;
    font-size: 2em;
    color: black;
    height: 15%;
    width: 100%;
    padding-left: 20px;
    padding-top: 10px;
    border-left-style: solid;
    border-left-width: 3px;
    border-left-color: #c62034;
    border-top-left-radius: 1vw;
}
.form_card_main_column {
    display: flex;
    flex-direction: column;
    width: 100%;
    border-radius: 1vw;
}
.form_card {
    height: 70%;
    width: 50%;
    border-color: grey;
    border-radius: 1vw;
    border-width: 3px;
    background-color: whitesmoke;
    display: flex;
    flex-direction: row;
    justify-content: center;
    margin-top: 5vw;
}
.form_container {
    height: 100%;
    width: 100%;
    background-color: transparent;
    display: flex;
    flex-direction: row;
    justify-content: center;
}
.icon_outline {
    border-style: solid;
    border-radius: 50%;
    border-width: 3px;
    border-color: white;
    height: 3vw;
    width: 3vw;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    margin-top: 2vh;
    margin-left: 2vw;
    transition: background-color 1s ease;
}
.icon_outline:hover {
    background-color: white;
    transition: background-color 1s ease;
}
.return_home_icon {
    width:90%;
    height:90%;
    color:white;
    border-radius: 50%;
    transition: color 1s ease, background-color 1s ease;
}
.return_home_icon:hover {
    color: #c62034;
    transition: color 1s ease;
}

.nav {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: flex-start;
    height: 11%;
    width: 100%;
    background-color: transparent;
}
.background {
    display: flex;
    flex-direction: column;
    justify-content: center;
    height: 100vh;
    width: 100%;
    position: relative;
    z-index: 3;
}
.layer_one {
    position: fixed;
    width: 0; 
    height: 0; 
    border-top: 40vw solid rgba(32, 40, 68, 1); 
    border-right: 20vw solid transparent;
    z-index: -1;
    display: flex;
}
.layer_two {
    bottom: 0;
    width: 0; 
    height: 0; 
    border-bottom: 35vw solid #c62034; 
    border-right: 20vw solid transparent; 
    position: fixed;
    z-index: 0;
}
.layer_three {
    position: fixed;
    width: 100vw; 
    height: 100vh;
    z-index: -4;
    display: flex;
    justify-content: flex-end;
    font-size: 3rem;
}
</style>