<script>
export default {
    name: 'ReviewSection',
    data() {
        return {
            subject_1: [
                {
                    title_1: 'it\'s a choice of quality for people with special needs',
                    review_1: 'I\'m very strict person so I require everything to be organized and neat. Then I\'ll be able to make things right and shine. MaxCoach guys just got me ',
                    image_1: '/testimonial-avata-03.jpg',
                    name_1: 'FLORENCE THEMES',
                    job_1: '/Multimedia Admin'
                }
            ],

            subject_2: [
                {
                    title_2: 'High level of efficiency and scientific teaching methods',
                    review_2: 'I am free to leanr at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus.Great study portal for people like me.',
                    image_2: '/testimonial-avata-02.jpg',
                    name_2: 'MINA HOLLACE',
                    job_2: '/Freelancer'
                },
            ],

            subject_3: [
                {
                    title_3: 'Professional team of specialists and passionate mentors at reach',
                    review_3: 'I need to get a certification for English proficiency and MaxCoach is my best  choice. Their tutors are smart and professional when dealing with students.  ',
                    image_3: '/testimonial-avata-04.jpg',
                    name_3: 'MADLEY PONDOR',
                    job_3: '/IT Specialist'
                }
            ]

        }
    }
}
</script>

<template>
    <div class="contain">
        <div class="text">
            <h3>
                People are praising Maxcoach
            </h3>
            <h1>What make they love us?</h1>
        </div>

        <div class="presentation">
            <div class="opacity-card" v-for="subject in subject_1">
                <h3 class="title">{{ subject.title_1 }}</h3>
                <p>{{ subject.review_1 }}</p>

                <div class="wrap-img">
                    <img :src="subject.image_1" alt="testimonial 1" class="wrapped">
                </div>
                <div class="box">
                    <h4>{{ subject.name_1 }}</h4>
                    <div class="job">{{ subject.job_1 }}</div>
                </div>

            </div>


            <div class="not-opacity" v-for="person in subject_2">
                <h3 class="title">{{ person.title_2 }}</h3>
                <p>{{ person.review_2 }}</p>
                <div class="wrap-img">
                    <img :src="person.image_2" alt="testimonial 2" class="wrapped">
                </div>
                <div class="box">
                    <h4>{{ person.name_2 }}</h4>
                    <div class="job"></div>{{ person.job_2 }}
                </div>
            </div>

            <div class="opacity-card" v-for="review in subject_3">
                <h3 class="title">{{ review.title_3 }}</h3>
                <p>{{ review.review_3 }}</p>
                <div class="wrap-img">
                    <img :src="review.image_3" alt="testimonial 3" class="wrapped">
                </div>
                <div class="box">
                    <h4>{{ review.name_3 }}</h4>
                    <div class="job"> {{ review.job_3 }}</div>
                </div>
            </div>

        </div>
        <div class="circles">
            <i class="fa-solid fa-circle first"></i>
            <i class="fa-regular fa-circle margin"></i>
            <i class="fa-regular fa-circle"></i>
            <i class="fa-regular fa-circle margin"></i>
        </div>
    </div>
</template>


<style scoped lang="scss">
@use '../styles/generals.scss' as *;

.contain {
    background-color: $secondary_background;
    padding: 10px;
    margin-top: 70px;
    min-height: 500px;
}

.text {
    text-align: center;

    h3 {
        color: $primary_color;
    }
}

.presentation {
    width: calc(100/ 3);
    display: flex;
    justify-content: space-around;
}

.title,
h4 {
    color: $hover_color;
}

.wrap-img {
    width: 80px;
    float: left;
    margin-right: 20px;

    .wrapped {
        width: 100%;
        border-radius: 50%;
    }
}

.opacity-card,
.not-opacity {
    margin: 10px 20px;
    padding: 10px;
}

.opacity-card {
    background-color: $background;
    opacity: 40%;
}

.not-opacity {
    background-color: white;
}

.circles {
    text-align: center;
    font-size: 8px;
    margin-top: 1rem;
    cursor: pointer;
    padding: 10px;

    .first {
        color: $hover_color;
    }

    .margin {
        margin: 0 10px;
    }
}
</style>