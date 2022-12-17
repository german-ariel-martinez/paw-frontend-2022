<template>
    <div class="grid">
        <div class="myreservations-title">
            <span>My reservations</span>
        </div>
        <div class="myreservations">

        </div>
        <div class="pendingtoreview-title">
            <span>Pending to review</span>
        </div>
        <div class="pendingtoreview">

        </div>
    </div>
</template>

<style scoped>
.grid {
    display: grid;
    grid-template-columns: repeat(11, 1fr);
    grid-template-rows: repeat(11, 1fr);
    height: 100%;
    background-image: url('~@/assets/adventure2.jpeg');
}
.myreservations-title span{
    background-color: #202844;
    color: white;
    border-top: 2px solid #c62034;
    border-bottom: 2px solid #c62034;
}
.myreservations-title {
    grid-column: 2/3;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
}
.pendingtoreview-title span{
    background-color: #202844;
    color: white;
    border-top: 2px solid #c62034;
    border-bottom: 2px solid #c62034;
}
.pendingtoreview-title {
    grid-column: 7/9;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
}
.myreservations {
    grid-column: 2/6;
    grid-row: 2/11;
    background-color: white;
    height: 100%;
}
.pendingtoreview {
    grid-column: 7/11;
    grid-row: 2/11;
    background-color: white;
    height: 100%;
}
</style>