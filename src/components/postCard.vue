<template>
    <div class="post">
        <div class="pic">
            <img class="pic-img" src="../assets/explore.jpg" alt="">
            <button class="btn" type="button">View Post</button> 
        </div>
        <div class="data">
            <div class="box1"><b-icon icon="geo-alt" style="color: white;margin-right:5px;"></b-icon> {{this.location}}</div>
            <div class="box2"><b-icon icon="volume-up" style="color: white;margin-right:5px;"></b-icon> {{this.languages}}</div>
            <div class="box3">{{this.rating}}<b-icon icon="star-fill" style="color: gold;margin-left:5px;padding-bottom:5px"></b-icon></div>
        </div>
    </div>
</template>

<style scoped>
.box1 {
    grid-column-start: 1;
    grid-column-end: 1;
    grid-row-start: 1;
    grid-row-end: 1;
}
.box2 {
    grid-column-start: 1;
    grid-column-end: 1;
    grid-row-start: 2;
    grid-row-end: 2;
}
.box3 {
    grid-column-start: 2;
    grid-column-end: 2;
    grid-row-start: 1;
    grid-row-end: 3;
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
    align-items: center;
    font-size: 2em;
    height: 100%;
    width: 100%;
    margin: 0;
    padding: 0;
}
.btn {
    position: absolute;
    top: 5%;
    right: 2.5%;
    border: none;
    outline: none;
    height: 40px;
    color: white;
    background-color: #c62034;
    font-size: 18px;
    border-radius: 20px;
    transition: all 1s ease;
}
.btn:hover {
    background-color: white;
    transition: all 1s ease;
    color: #c62034;
}
.pic-img {
    float: left;
    width: 100%;
    height: 100%;
    object-fit: cover;
}
.pic {
    display: flex;
    flex-direction: row;
    width: 100%;
    height: 70%;
}
.data {
    display: grid;
    grid-template-columns: 2fr 1fr;
    grid-template-rows: 1fr 1fr;
    align-items: center;
    justify-items: flex-start;
    color: white;
    width: 95%;
    height: 30%;
}
.post {
    position: relative;
    background-color: #202844;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 3vh;
    margin-bottom: 3vh;
    width: 35vw; 
    height: 35vh;
}
</style>

<script>
export default {
    props: {
        location: String,
        languages: String,
        rating: Number
        // pid: Number
    }
}
</script>