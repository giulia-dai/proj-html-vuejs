<script>
export default {
    name: 'VideoSection',
    data() {
        return {

        }
    }
}
</script>

<template>
    <div class="contain">
        <div class="img-wrap">
            <img class="wrapped" src="../assets/images/home-business-video-poster-670x450.jpg" alt="video">
            <img class="youtube" src="../assets/images/icon-youtube-play.png" alt="logo youtube">
        </div>
    </div>
</template>


<style scoped lang="scss">
@use'../styles/generals.scss' as *;

.contain {
    background-color: $hover_color;
    background-image: url(../assets/images/background-map-dots-top-right-transparent.png);
    background-repeat: no-repeat;
    background-position: right;
    background-size: 720px;
    background-position-y: top;
    min-height: 600px;
}

.img-wrap {
    width: 550px;
    position: relative;

    .wrapped {
        width: 100%;
        position: absolute;
        left: 100px;
        top: 120px;
        border-radius: 10px;
    }

    .youtube {
        position: absolute;
        left: 315px;
        top: 270px;
        cursor: pointer;
    }
}
</style>