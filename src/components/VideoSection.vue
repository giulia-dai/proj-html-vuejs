<script>
export default {
    name: 'VideoSection',
    data() {
        return {
            items: [
                {
                    icon: 'fa-solid fa-circle-chevron-down',
                    subtitle: 'Why would I need a Business COACH?',
                },
                {
                    icon: 'fa-solid fa-circle-chevron-down',
                    subtitle: 'What is one-on-one coaching?'
                }
            ]

        }
    }
}
</script>

<template>
    <div class="contain">
        <!-- video youtube -->
        <div class="img-wrap">
            <img class="wrapped" src="../assets/images/home-business-video-poster-670x450.jpg" alt="video">
            <img class="youtube" src="../assets/images/icon-youtube-play.png" alt="logo youtube">
        </div>

        <!-- immagine sotto al video -->
        <div class="size">
            <img class="size-shape" src="../assets/images/maxcoach-shape-07-100x100.png">
        </div>


        <!-- angolo domande -->

        <div class="box">
            <h1 class="title">To Thrive In Business Today, You'll Nedd a Good Plan</h1>
            <div class="big-text">
                <i class="fa-solid fa-circle-chevron-up green-icon"></i>
                <h3 class="green-title">How can we help?</h3>
                <div class="paragraph">
                    <p>How many courses you\'ve been on, using however many techniques and methods.Unless you\'ve yet to
                        understand how success comes.</p>
                    <p>With everyone else\'s mindset involved impacting too. Hence why business coaching is so crucial
                        for
                        success.</p>
                </div>
            </div>
            <div class="faq" v-for="item in items">
                <div :class="item.icon" class="icons"></div>
                <h3 class="small-title">{{ item.subtitle }}</h3>
            </div>
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
    background-size: 730px;
    background-position-y: top;
    min-height: 600px;
    position: relative;
    margin-top: 40px;
}

.size {
    width: 130px;
    position: relative;

    .size-shape {
        width: 100%;
        position: absolute;
        top: 460px;
        left: 55px;
    }

}

.img-wrap {
    width: 520px;
    position: relative;
    z-index: 999;


    .wrapped {
        width: 100%;
        position: absolute;
        left: 140px;
        top: 120px;
        border-radius: 10px;
    }

    .youtube {
        position: absolute;
        width: 85px;
        left: 355px;
        top: 270px;
        cursor: pointer;
    }
}

.title {
    color: white;
}

.box {
    position: absolute;
    right: 270px;
    top: 50px;
    max-width: 360px;
}


.green-title {
    color: $primary_color;
}

.small-title {
    color: white;
    border-bottom: 1.5px solid #484657;
    padding-bottom: 15px;
}

.big-text {
    border-bottom: 1.5px solid #484657;
    padding-bottom: 15px;
}

.paragraph {
    margin-left: 40px;
    color: white;
}

.green-icon {
    color: $primary_color;
    float: left;
    padding-right: 20px;
    font-size: 20px;
}

.icons {
    float: left;
    font-size: 20px;
    padding-right: 20px;
    color: white;
}
</style>