<script>
export default {
    name: 'FooterTop',
}
</script>

<template>
    <div class="contain">

        <!-- testo -->
        <div class="text">
            <div class="size">
                <div><strong>Subscribe</strong>
                    <a class="green" href="#"> Newsletter</a>
                </div>
            </div>
            <div class="adv-txt">
                <p>Enter your email address to register to our newsletter subscription <br> delivered on a regular basis!
                </p>
            </div>

            <!-- form -->
            <form>
                <input type="email" class="mail" placeholder="Enter your email">
                <button>Subscribe</button>
            </form>
            <!-- immagini sfondo -->
            <div class="bg">
                <div class="img-wrap">
                    <img src="../assets/images/maxcoach-shape-02.png" alt="" class="wrapped">
                </div>
            </div>
            <div class="second-img">
                <img class="second-wrap" src="../assets/images/blu-vert-circle.png" alt="circle">
            </div>
        </div>

    </div>
</template>

<style lang="scss" scoped>
@use '../styles/generals.scss' as *;

.contain {
    margin-top: 60px;
    min-height: 300px;
}

.text {
    text-align: center;
    position: relative;


    .size {
        font-size: 35px;
    }

    .green {
        color: $primary_color;
        text-decoration: none;
    }
}

.mail {
    margin-top: 2rem;
    padding: 15px;
    border-top-left-radius: 5px;
    border-bottom-left-radius: 5px;
    border: none;
    background-color: $secondary_background;
    width: 400px;
}

button {
    padding: 15px;
    color: white;
    background-color: $primary_color;
    border: 1px solid $border_color;
    border-top-right-radius: 5px;
    border-bottom-right-radius: 5px;
    margin-left: 3px;
    cursor: pointer;
}

.bg {
    min-width: 170px;
    min-height: 170px;
    position: absolute;
    top: 0px;
    right: 180px;
    background-image: url(../assets/images/maxcoach-shape-09.png);
    background-repeat: no-repeat;
    background-size: 170px;
}

.img-wrap {
    width: 100px;
    position: relative;

    .wrapped {
        width: 100%;
        position: absolute;
        top: 70px;
        right: -60px;
    }
}

.second-img {
    position: relative;
    width: 50px;

    .second-wrap {
        width: 100%;
        position: absolute;
        bottom: 70px;
        right: -200px;
    }
}
</style>