<script>
export default {
    name: 'HelpSection',
    data() {
        return {
            items: [
                {
                    image: '/home-business-service-slide-01-480x298.jpg',
                    title: 'Consultative Training',
                    text: 'With a coach addressing multiple issues that are off balance, affecting your business in various unconsidered ways.'
                },
                {
                    image: '/home-business-service-slide-02-480x298.jpg',
                    title: 'Real Deal Coaching',
                    text: 'Brings an exeptionally powerful opportunity. Being abòle to accept,to work with that opportunity.'

                },
                {
                    image: '/home-business-service-slide-03-480x298.jpg',
                    title: 'Advisor Training Program',
                    text: 'Getting high quality, entrepreneur mindset driven online business coaching, is what is needed.'
                }
            ],
        }
    }
};
</script>


<template>
    <div class="box">
        <div class="text">
            <h4>Let's Dream Big Together</h4>
            <h2>Explore How can I help you</h2>
        </div>

        <div class="second-box">
            <div v-for="item in items" class="card" style="width: 20rem;">
                <img :src="item.image" class="card-img-top" alt="">

                <div class="card-body">
                    <h3>{{ item.title }}</h3>
                    <p class="card-text">{{ item.text }}</p>
                </div>

                <div class="card-end">
                    <h4 class="discover">Discover now <i class="fa-solid fa-arrow-right"></i> </h4>
                </div>
            </div>
        </div>
    </div>
</template>


<style scoped lang="scss">
@use '../styles/generals.scss' as *;

.box {
    background-color: $secondary_background;
    min-height: 500px; //misura da modificare dopo eventualmente!!
    margin-top: 50px;
}

.text {
    padding-top: 30px;
    text-align: center;

    h4 {
        color: $primary_color;
    }
}

.second-box {
    display: flex;
    justify-content: center;
}

.card {
    width: calc(100% / 3);
    margin: 10px;
    text-align: center;
}

img {
    width: 100%;
    border: 0.5px solid black;
    border-top-right-radius: 5px;
    border-top-left-radius: 5px;
}

.card-body {
    padding: 10px;
    border-left: 1.5px solid #EFEFEF;
    border-right: 1.5px solid #EFEFEF;
}

.card-end {
    color: $primary_color;
    border-bottom-left-radius: 5px;
    border-bottom-right-radius: 5px;
    border: 1.5px solid #EFEFEF;

    &:hover {
        color: white;
        background-color: $primary_color;
        cursor: pointer;
    }
}
</style>