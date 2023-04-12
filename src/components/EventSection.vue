<script>
export default {
    name: 'EventSection',
    data() {
        return {
            items: [
                {
                    icon: 'fa-solid fa-location-dot',
                    country: 'Texas,US',
                    title: 'Storytelling Workshop',
                    day: '22',
                    month: 'NOV',
                    ticket: 'Get ticket'
                },
                {
                    icon: 'fa-solid fa-location-dot',
                    country: 'New York, US',
                    title: 'Painting Art Contest 2020',
                    day: '10',
                    month: 'OCT',
                    ticket: 'Get ticket'
                },
                {
                    icon: 'fa-solid fa-location-dot',
                    country: 'Hamburg, Germany',
                    title: 'International Art Fair 2020',
                    day: '23',
                    month: 'NOV',
                    ticket: 'Get ticket'
                },
                {
                    icon: 'fa-solid fa-location-dot',
                    country: 'illinois,US',
                    title: 'Street Perfonmance:Call for Artist',
                    day: '15',
                    month: 'DEC',
                    ticket: 'Get ticket'
                },
                {
                    icon: 'fa-solid fa-location-dot',
                    country: 'Illinois,US',
                    title: 'Consumer Food Safety Education Conference',
                    day: '22',
                    month: 'JUL',
                    ticket: 'Get ticket'
                },
                {
                    icon: 'fa-solid fa-location-dot',
                    country: 'Dubai',
                    title: 'How meditation improve your mental health?',
                    day: '12',
                    month: 'AUG',
                    ticket: 'Get ticket'
                }
            ],
        };
    }
}
</script>

<template>
    <div class="contain">
        <div class="box">
            <h4>Wanna transform your life?</h4>
            <h1>Upcoming Events</h1>
        </div>

        <div class="box_2">
            <!-- parte sinistra della card -->
            <div v-for="item in items" class="card">
                <div :class="item.icon" class="icons"> </div>
                <h5 class="place">{{ item.country }}</h5>
                <h3 class="event">{{ item.title }}</h3>

                <!-- parte destra della card -->
                <div class="right">
                    <div class="day">{{ item.day }}</div>
                    <div class="month">{{ item.month }}</div>
                    <button class="ticket">{{ item.ticket }}</button>
                </div>
            </div>
        </div>
        <div class="discover">Excited about our event?
            <a href="#"> View all events
                <i class="fa-solid fa-arrow-right"></i>
            </a>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use '../styles/generals.scss' as *;

.contain {
    margin-top: 40px;
    padding: 10px;
}

.box {
    text-align: center;

    h4 {
        color: $primary_color;
    }
}

.box_2 {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;

}

.card {
    background-color: $secondary_background;
    margin: 10px;
    width: calc(100% / 3);
    float: left;
    padding: 15px;
    position: relative;
}

.event {
    max-width: 300px;
}

.place {
    color: #9A9A9A;
    font-weight: 200;
}


.icons {
    float: left;
    font-size: 13px;
    margin-top: 20px;
    padding-right: 10px;
    color: #9A9A9A;
}

.right {
    float: right;
    position: relative;
    text-align: center;
    position: absolute;
    right: 10px;
    top: 25px;
}

.day {
    font-size: 35px;
    color: $primary_color;
}

.month {
    font-weight: 500;
    font-size: 14px;
}

.ticket {
    width: 130px;
    padding: 7px;
    color: white;
    background-color: $primary_color;
    border: $border_color;
    border-radius: 3px;
    cursor: pointer;

    &:hover {
        background-color: $hover_color;
        border: black;
    }
}

.discover {
    text-align: center;

    a {
        color: $primary_color;
        font-weight: 600;
    }
}
</style>