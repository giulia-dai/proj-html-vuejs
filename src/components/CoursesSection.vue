<script>
export default {
    name: 'CoursesSection',
    data() {
        return {
            items: [
                {
                    image: '/course-02-443x600.jpg',
                    price: '$40.',
                    small_price: '00',
                    title: 'Learning to Write as a Professional Author'
                },
                {
                    image: '/stock-full-hd-03-443x600.jpg',
                    price: 'Free',
                    title: 'Customer-centric Info-Tech Strategies'
                },
                {
                    image: '/stock-full-hd-04-443x600.jpg',
                    price: '$19.',
                    small_price: '00',
                    title: 'Open Programming Courses for Everyone: Pyton'
                },
                {
                    image: '/stock-full-hd-06-443x600.jpg',
                    price: '$26.',
                    small_price: '00',
                    title: 'Academic Listening and Note-taking'
                }
            ],

        };
    },
};
</script>
<template>
    <div class="box">
        <div class="text">
            <h4>Let's Dream Big Together</h4>
            <h2>Explore How can I help you</h2>
        </div>
    </div>
    <div class="second-box">
        <div v-for="item in items" class="card" style="width: 20rem;">
            <img :src="item.image" alt="">
            <div class="end">
                <h2 class="price">{{ item.price }}
                    <span class="cents">{{ item.small_price }}</span>
                </h2>
                <h3 class="course">{{ item.title }}</h3>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use '../styles/generals.scss' as *;

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
    width: calc(100% / 4);
    position: relative;
    margin: 0 10px;

}

img {
    width: 100%;
}


.end {
    position: absolute;
    bottom: 5px;
    background-color: #0000005f;
    padding-left: 20px;
}

.price {
    color: $primary_color;
    margin-bottom: -15px;

    .cents {
        font-size: 14px;
    }
}

.course {
    color: white;
}
</style>