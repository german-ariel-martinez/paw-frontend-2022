<template>
    <div class="bg">
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
                            <button class="btn" type="button" @click="validateForm()"> Finish </button>
                        </div>
                        <div class="form_form">
                            <form class="form_main_col" name="myForm">
                                <div class="form_row">
                                    <!-- email -->
                                    <input class="form_input" v-model="email" type="text" id="fname" name="email" placeholder="Enter your email">
                                    <span class="error-message" v-show="!v_email">Email is not valid.</span>
                                </div>
                                <div class="form_row_2">
                                    <div class="form_col" style="margin-right:5%;">
                                        <!-- pass 1 -->
                                        <input class="form_input" v-model="pass" type="password" id="fname" name="firstname" placeholder="Enter your password">
                                        <span class="error-message" v-show="!v_pass">Password must be at least 8 characters long.</span>
                                    </div>
                                    <div class="form_col">
                                        <!-- pass 2 -->
                                        <input class="form_input" v-model="cpass" type="password" id="fname" name="firstname" placeholder="Confirm password">
                                        <span class="error-message" v-show="!v_cpass">Passwords don't match.</span>
                                    </div>
                                </div>
                                <div class="form_row_2">
                                    <div class="form_col" style="margin-right:5%;">
                                        <!-- name -->
                                        <input class="form_input" v-model="name" type="text" id="fname" name="firstname" placeholder="Enter your name">
                                        <span class="error-message" v-show="!v_name_chars">May only contain letters, spaces, accents and apostrophes.</span>
                                        <span class="error-message" v-show="!v_name_len">Should be at least 2 characters long.</span>
                                    </div>
                                    <div class="form_col">
                                        <!-- last name -->
                                        <input class="form_input" v-model="lastname" type="text" id="fname" name="firstname" placeholder="Enter your lastname">
                                        <span class="error-message" v-show="!v_lastname_chars">May only contain letters, spaces, accents and apostrophes.</span>
                                        <span class="error-message" v-show="!v_lastname_len">Should be at least 2 characters long.</span>
                                    </div>
                                </div>
                                <div class="form_row_3">
                                    <!-- desc -->
                                    <textarea class="form_textarea" v-model="desc" name="textarea" placeholder="Just a brief description about you..."></textarea>
                                    <span class="error-message" v-show="!v_desc">A brief description is required.</span>
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
            email : '',
            pass : '',
            cpass : '',
            name : '',
            lastname : '',
            desc : '',
            v_email : true,
            v_pass : true,
            v_cpass : true,
            v_name_chars : true,
            v_name_len : true,
            v_lastname_chars : true,
            v_lastname_len : true,
            v_desc : true,
        }
    },
    methods: {
        goto: function(to) {
            this.$router.push({name:to});
        },
        validateForm: function() {
            console.log("Pass : " + this.pass)
            console.log(String(this.pass).length)
            if (!this.validateEmail())
                this.v_email = false
            else
                this.v_email = true
            if (String(this.pass).length < 8)
                this.v_pass = false
            else
                this.v_pass = true
            if (this.pass != this.cpass || this.cpass == '')
                this.v_cpass = false
            else
                this.v_cpass = true
            if (String(this.name).length < 2)
                this.v_name_len = false
            else
                this.v_name_len = true
            if (/\d/.test(this.name))
                this.v_name_chars = false
            else
                this.v_name_chars = true
            if (String(this.lastname).length < 2)
                this.v_lastname_len = false
            else
                this.v_lastname_len = true
            if (/\d/.test(this.lastname))
                this.v_lastname_chars = false
            else
                this.v_lastname_chars = true
            if (this.desc == '')
                this.v_desc = false
            else
                this.v_desc = true
            // goto(feed)
        },
        validateEmail: function() {
            return this.email.match(/^[a-zA-Z0-9.!#$%&'*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*$/)
        }
    }
}
</script>

<style scoped>
.bg {
    background-image: url('~@/assets/mountain.jpg');
    background-size: cover; /* or contain depending on what you want */
    background-position: center center;
    background-repeat: no-repeat;
    text-align:center;
    margin:auto;
    padding:0;
    transition: all 1s ease;
}
.btn:hover {
    background-color: #c62034;
    transition: all 1s ease;
    color: white;
}
.btn {
    border: none;
    outline: none;
    height: 40px;
    color: white;
    background-color: rgba(32, 40, 68, 1);
    font-size: 18px;
    margin-right: 20px;
}
.error-message {
    color:#c62034;
    font-size: 1.5vh;
}
.asd {
    margin-right:2vw;
    margin-top:1.5vh;
    color:white;
    border-bottom: 5px solid #c62034;
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
    background-color: white;
}
.form_row_3 {
    display: flex;
    flex-direction: column;
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
    flex-direction: column;
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
    background-color: white;
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
    justify-content: space-between;
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
    display: flex;
    justify-content: flex-end;
    font-size: 3rem;
    background-color: rgba(32, 40, 68, 1);
}
</style>