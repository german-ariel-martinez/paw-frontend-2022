<template>
    <div class="profile-layout">
        <div class="profile-data">
            <div class="pic-n-name">
                <div class="pic">
                    <img class="img" src="https://shotkit.com/wp-content/uploads/2021/06/cool-profile-pic-matheus-ferrero.jpeg" alt="">
                </div>
                <div class="name">
                    Milagros Moutin
                </div>
                <button class="btn" type="button"><b-icon icon="pencil-square" style="padding-bottom: 3px; margin-right:2px"></b-icon>Edit profile</button>
            </div>
            <div class="rating">
                <div>
                    4.7
                    <b-icon icon="star-fill" style="color: gold;"></b-icon>
                </div>
                <div style="font-size:2em;">Rated 17 times</div>
            </div>
            <div class="about">
                <div class="desc-title">
                    <span> About me... </span>
                </div>
                <div class="description">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum pariatur tenetur aliquid at, eos perferendis totam consectetur illum, repellat aliquam quaerat, maiores voluptate aspernatur vel reprehenderit voluptas eius laudantium nulla?
                    Ipsam earum distinctio vitae? Facere harum facilis, voluptatibus quasi dolorem dicta est pariatur maxime nobis illum exercitationem at unde, mollitia adipisci ipsum, laborum a similique iste obcaecati assumenda qui error!
                    Rem debitis laborum adipisci maiores! Molestias animi iure repudiandae cupiditate similique praesentium laboriosam, enim, labore maxime assumenda exercitationem perspiciatis officia quos cum tenetur perferendis. Voluptas quisquam magni accusamus earum eum.
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.desc-title span{
    background-color: #202844;
    color: white;
}
.desc-title {
    grid-column: 2/3;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
}
.description {
    grid-column: 2/8;
    grid-row: 2/8;
    background-color: rgba(0,0,0,0.1);
    text-align: justify;
    padding: 1vw 1vw;
}
.about {
    display: grid;
    grid-template-columns: repeat(8, 1fr);
    grid-template-rows: repeat(8, 1fr);
    height: 60%;
}
.rating div:first-child {
    border-right: 2px solid rgba(0,0,0,0.1);
}
.rating div {
    display: inline;
    flex-direction: column;
    width: 50%;
    font-size: 7vh;
}
.rating {
    display: flex;
    flex-direction: row;
    height: 15%;
    justify-content: center;
    align-items: center;
    border-bottom: 2px solid #c62034;
}
.profile-layout {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    height: 100%;
    background-color: rgba(0,0,0,0.1);
    background-image: url('~@/assets/adventure2.jpeg');
}
.profile-data {
    background-color: whitesmoke;
    grid-column: 2/5;
    width: 100%;
    display: flex;
    flex-direction: column;
}
.pic-n-name {
    display: flex;
    flex-direction: row;
    height: 25%;
    justify-content: space-around;
    align-items: center;
    background-color: #202844;
    color: white;
}
.pic {
    width: 10vw;
    height: 10vw;
    position: relative;
    overflow: hidden;
    border-radius: 50%;
    border: 5px solid #c62034;
    display: flex;
    flex-direction: column;
}
.img {
    display: flex;
    flex-direction: column;
    margin: 0 auto;
    margin-left: -25%;
    height: 100%;
    width: auto;
}
.btn {
    border: none;
    outline: none;
    height: 5vh;
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
.name {
    display: flex;
    flex-direction: column;
    font-size: 3em;
}
</style>