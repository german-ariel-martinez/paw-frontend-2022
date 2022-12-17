<template>
    <div class="post-viewer">
        <div class="user-info">
            <div class="user-display">
                <div class="usr-img">
                    <img class="img" src="https://shotkit.com/wp-content/uploads/2021/06/cool-profile-pic-matheus-ferrero.jpeg" alt="">
                </div>
                <div class="usr-info2">
                    <div class="usr-name">Milagros Moutin</div>
                    <div>This user has been rated 17 times</div>
                    <div>Rated 4.7/5<b-icon icon="star-fill" style="color: gold;padding-left: 2px;padding-bottom: 2px;"></b-icon></div>
                </div>
            </div>
        </div>
        <div class="post-info">
            <div> Apartment in Puerto Madero by the river. Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi at, aspernatur corporis nisi corrupti quia aut sapiente dolore vel placeat accusamus voluptatum nemo quae alias recusandae, illum dicta. Vero, nihil.</div>
            <div> This post has not been reviewed yet.</div>
            <div> We speak: English, Spanish.</div>
            <div>This place offers:</div>
            <div style="margin-top: 0"> 
                <ul>
                    <li>Pool</li>
                    <li>Pets</li>
                    <li>Wifi</li>
                </ul>
            </div>
        </div>
        <div class="application-info">
            <div class="application-form">
                <div> Arrival <input class="date-picker" type="date" > Departure <input class="date-picker" type="date" ></div>
                <div><textarea class="app-text" placeholder="Message"></textarea></div>
                <div><button class="btn" type="button">Apply to this post!</button></div>
            </div>
        </div>
        <div class="img-display"></div>
    </div>
</template>

<style scoped>
/* Parte del usuario ----------------------------- */
.usr-name {
    font-size: 2em;
}
.usr-info div {
    display: flex;
    flex-direction: row;
}
.usr-info2 {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    width: 50%;
    height: 100%;
}
.usr-img {
    width: 10vw;
    height: 10vw;
    position: relative;
    overflow: hidden;
    border-radius: 50%;
}
.img {
    display: flex;
    flex-direction: column;
    margin: 0 auto;
    margin-left: -25%;
    height: 100%;
    width: auto;
}
.user-display {
    display: flex;
    flex-direction: row;
    height: 100%;
    width: 100%;
    justify-content: space-around;
    align-items: center;
}
.user-info {
    grid-column: 1/4;
    width: 100%;
    height: 100%;
    border-bottom-style: solid;
    border-bottom-width: 2px;
    border-bottom-color: #c62034;
}
/*  Parte de informacion del post ---------------------------------- */
.post-info {
    grid-column: 1/4;
    grid-row: 2/4;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    overflow-y: scroll;
}
.post-info div {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    width: 90%;
    align-self: center;
    text-align: justify;
    margin-top: 3vh;
}
.post-info div:last-child {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    width: 90%;
    align-self: center;
    text-align: justify;
}
/* Parte de aplicacion ---------------------------------------- */
.date-picker {
    color: white;
    border: 1px solid white;
    margin: 0 1vw;
}
::-webkit-calendar-picker-indicator {
    filter: invert(1);
    margin-right: .15vw;
}
::-webkit-datetime-edit { 
    padding: .25vw; 
}
.app-text {
    color: white;
    border: 1px solid white;
    width: 100%;
    margin: 1vh;
    padding: .5vw .5vw;
}
.application-info {
    background-color: #202844;
    grid-column: 1/4;
    grid-row: 4/5;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
.application-form div {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    width: 100%;
}
.application-form {
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 95%;
    justify-content: center;
    align-items: center;
    border-top-style: solid;
    border-bottom-style: solid;
    border-top-color: white;
    border-top-width: 2px;
    border-bottom-color: white;
    border-bottom-width: 2px;
    color: white;
}
.btn {
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
.img-display {
    background-color: #bebfc2;
    grid-column: 4/8;
    grid-row: 1/5;
    width: 100%;
    height: 100%;
}
.post-viewer {
    display: grid;
    grid-template-columns: repeat(7, 1fr);
    grid-template-rows: repeat(4, 1fr);
    height: 100%;
}
</style>