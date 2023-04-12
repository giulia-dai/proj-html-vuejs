<script>
export default {
    name: 'AboutUsSection',
    data() {
        return {
            items: [
                {
                    icon: 'fa-solid fa-headset',
                    title: 'One to One',
                    subtitle: 'Getting the necessary clarity about the current state to help you improve your game. '
                },
                {
                    icon: 'fa-solid fa-location-dot',
                    title: 'Anywhere',
                    subtitle: 'Access to valuable and portable program which allow you to setup and live anywhere you want.'
                },
                {
                    icon: 'fa-regular fa-clock',
                    title: 'On Time',
                    subtitle: 'Punctuality is our top priority because it\'s an essential criteria to assess  a program quaality.'
                },
                {
                    icon: 'fa-solid fa-display',
                    title: 'Online Courses',
                    subtitle: 'Online business coaching now offers you a very powerfull way to empower your business into success.'
                },
                {
                    icon: 'fa-solid fa-user-tie',
                    title: 'Consulting',
                    subtitle: 'You will get a clear sense of direction for your business, thorough assessment and faster results.'
                },
                {
                    icon: 'fa-solid fa-gear',
                    title: 'Self Development',
                    subtitle: 'Business Coaching often keep your focus and develop you both in a professional and personal way.'
                }
            ]


        }
    }
}
</script>
<template>
    <div class="box">
        <div class="text-wrap">
            <div class="text">
                <h4>Let's Dream Big Together</h4>
                <h2>We are pioneers of the digital approach, using leading-edge technology to semplify procedures and apply
                    executive coaching in the new age of digitalization
                </h2>
            </div>
        </div>
        <div class="second-box">
            <div v-for="item in items" class="presentation">
                <div :class="item.icon" class="icons"></div>
                <h3 class="mid-title">{{ item.title }}</h3>
                <div class="subt">{{ item.subtitle }}</div>
            </div>
        </div>
        <div class="btns">
            <button class="learn">Learn more</button>
            <button class="start">Get started today</button>
        </div>


    </div>
</template>
<style scoped lang="scss">
@use '../styles/generals.scss' as *;

.box {
    max-width: 1000px;
    margin: 0 auto;
}

.text-wrap {
    display: flex;
    justify-content: center;
}

.text {
    max-width: 650px;
    text-align: center;

    h4 {
        color: $primary_color;
    }
}

.second-box {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
}

.presentation {
    text-align: center;
    width: calc(100% / 4);
    float: left;
    margin: 10px 20px;


    .mid-title {
        text-align: left;
        float: left;
    }

    .subt {
        text-align: justify;
        float: left;
    }
}

.icons {
    float: left;
    font-size: 30px;
    margin-top: 10px;
    padding-right: 10px;
}

.btns {
    text-align: center;
    margin-top: 30px;
}

button {
    border-radius: 5px;
    padding: 10px;
    cursor: pointer;

    &:hover {
        border: black;
        background: $hover_color;
    }
}

.learn {
    color: $primary_color;
    background-color: white;
    border: 1px solid grey;
    width: 130px;
    margin-right: 20px;

    &:hover {
        color: white;
    }
}

.start {
    background-color: $primary_color;
    border: 1px solid $border_color;
    color: white;
    margin-top: 10px;
}
</style>