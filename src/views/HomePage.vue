<template>
<div style="height: 100%;">
    <!-- NAVBAR -->
    <div class="navbar">
        <div class="col1">
            <div class="brand">
                <b class="title"> Globepackers <b-icon icon="compass" style="color: white;margin-left: 10px"></b-icon></b>
            </div>
        </div>
        <div class="col2">
            <div class="links">
                <ul class="navbar_links">
                    <li><router-link class="link" to="/posts">Feed</router-link></li>
                    <li><router-link class="link" to="/reservations">Reservations</router-link></li>
                    <li><router-link class="link" to="/applications">Applications</router-link></li>
                    <li><router-link class="link" to="/signup">Profile</router-link></li>
                    <li><router-link class="link" to="/posts/feed">Log Out</router-link></li>
                </ul>
            </div>
        </div>
    </div>
    <!-- ELEMENTO VARIABLE -->
    <div class="changingElement">
        <router-view></router-view>
    </div>
</div>
</template>

<script>
export default {
    name: 'HomePage',
    methods: {
        Feed(){
            this.$router.push('/home/feed')
        },
        Vote(){
            this.$router.push('/home/vote')
        },
        CPost(){
            this.$router.push('/home/createpost')
        },
        sotm(){
            this.$router.push('/home/sotm')
        }
    }
}
</script>

<style scoped>
    .changingElement {
        overflow-y: scroll;
        display: flex;
        flex-direction: column;
        height: 92vh;
    }
    .col1 {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        justify-content: center;
        width: 50%;
        margin: 0;
        padding: 0;
    }
    .col2 {
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        width: 50%;
    }
    .navbar {
        background-color: #c62034;
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        height: 8vh;
        margin: 0;
        padding: 0;
    }
    .brand {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        width: 40%;
        height: 80%;
        border-style: solid;
        border-width: 3px;
        border-color: white;
        border-radius: 20px;
        margin-left: 1vw;
        color: white;
    }
    .title {
        cursor: pointer;
        font-size: 2em;
        margin-left: 10px;
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
    }
    .links {
        display: flex;
        flex-direction: row;
        justify-content: flex-end;
        align-items: center;
        width: 80%;
        height: 80%;
        margin-right: 10px;
        border-top-right-radius: 15px;
        border-bottom-right-radius: 15px;
    }
    .links:hover {
        color: white;
    }
    .navbar_links {
        list-style-type: none;
        display: flex;
        flex-direction: row;
        margin: 0;
    }
    .navbar_links li {
        display: inline-block;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        color: white;
        border-style: solid;
        border-left-style: none;
        border-width: 2px;
        transition: all 1s ease;
        height: 6vh;
        width: 10vw;
        transition: all 1s ease;
    }
    .navbar_links li:hover {
        background-color: white;
        transition: all 1s ease;
        color: white;
    }
    .navbar_links li a:hover {
        transition: all 1s ease;
        color: #c62034;
    }
    .link {
        height: 100%;
        width: 100%;
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        text-decoration: none;
        color: white;
        cursor: pointer;
    }
    .link a:hover {
        color: #c62034;
    }
    .navbar_links li:last-child {
        border-top-right-radius: 15px;
        border-bottom-right-radius: 15px;
    }
    .navbar_links li:first-child {
        border-top-left-radius: 15px;
        border-bottom-left-radius: 15px;
        border-left-style: solid;
    }
    
</style>