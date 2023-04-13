<script>
export default {
    name: 'FooterTop',
    data() {
        return {

        }
    }
}
</script>

<template>
    <div class="contain">

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
</style>