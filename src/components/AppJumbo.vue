<script>
export default {
    name: 'AppJumbo',

};
</script>

<template>
    <div class="jumbo">
        <div class="text">
            <h4>New Challenges, New Skills</h4>
            <h1>BUILD YOUR OWN LIFE COACHING BUSINESS</h1>
            <div>
                Whole-Life Business Coaching for committed entrepreneurs
            </div>
            <button>Get started today</button>
        </div>
        <div class="man">
            <img src="../assets/images/home-business-hero-avatar.png" alt="business man">
        </div>
    </div>
</template>

<style scoped lang="scss">
@use '../styles/generals.scss' as *;

.jumbo {
    background-image: url(../assets/images/home-business-hero-global-image.png);
    background-size: contain;
    background-position: 750px;
    background-repeat: no-repeat;
    background-color: $background;
    min-height: 400px;
    position: relative;
}

.text {
    max-width: 300px;
    position: absolute;
    left: 150px;
    top: 50px;

    h4 {
        color: $primary_color;
    }

    button {
        background-color: $primary_color;
        border: 1px solid $border_color;
        border-radius: 5px;
        padding: 10px;
        color: white;
        margin-top: 10px;
        cursor: pointer;

        &:hover {
            border: black;
            background: $hover_color;
        }

    }
}

.man {
    position: absolute;
    right: 250px;
    bottom: -5px;
    width: 22%;

    img {
        width: 100%;
    }
}
</style>