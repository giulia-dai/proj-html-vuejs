<script>
import FooterProps from './FooterProps.vue';
export default {
    name: 'FooterBottom',
    components: {
        FooterProps
    },
    data() {
        return {
            items: [
                {
                    title: 'Address',
                    address: '382 NE 191st # 87394 Miami, FL 33179-3899',
                    number: '+1(305)547-9909 (9am-5pm EST, Monday-Friday)',
                    mail: 'support@maxcoach.com'
                }
            ],
            elements: [
                {
                    big_title: 'Explore',
                    _1: 'Start here',
                    _2: 'Blog',
                    _3: 'About us'
                },
                {
                    big_title: '',
                    _1: 'Success story',
                    _2: 'Courses',
                    _3: 'Contact us'
                },
                {
                    big_title: 'Information',
                    _1: 'Membership',
                    _2: 'Purchase guide',
                    _3: 'Privacy policy',
                    _4: 'Terms of service'
                }
            ],
        }
    }
}
</script>

<template>
    <div class="contain">

        <div class="position">

            <div class="box">
                <FooterProps v-for="item in items" :big_title="item.title" :country="item.address" :phone="item.number"
                    :mail="item.mail" />

                <!-- icone social -->
                <div class="icons">
                    <i class="fa-brands fa-square-facebook"></i>
                    <i class="fa-brands fa-twitter"></i>
                    <i class="fa-brands fa-instagram"></i>
                    <i class="fa-brands fa-linkedin"></i>
                </div>
            </div>

        </div>

        <div class="menu">
            <ul class="lista" v-for="element in elements">
                <li>
                    <h3>{{ element.big_title }}</h3>
                </li>
                <li>{{ element._1 }}</li>
                <li>{{ element._2 }}</li>
                <li>{{ element._3 }}</li>
                <li>{{ element._4 }}</li>
            </ul>
        </div>
        <!-- copyright -->
        <div class="copyright">&#169; 2020 Maxcoach. All Rights Reserved</div>
        <button class="up">
            <a href="#courses"><i class="fa-solid fa-arrow-up-long"></i></a>
        </button>
    </div>
</template>

<style scoped lang="scss">
@use '../styles/generals.scss' as *;

.contain {
    min-height: 300px;
    background-color: black;
    position: relative;
}

.position {
    position: absolute;

    .box {
        position: relative;
        left: 80px;
        top: 30px;
    }
}

.icons .fa-brands {
    color: grey;
    padding: 10px;
    font-size: 30px;
    cursor: pointer;
}

.menu {
    position: absolute;
    right: 200px;
    top: 35px;
}

.lista {
    list-style: none;
    float: left;

    li {
        color: grey;
        line-height: 30px;

        h3 {
            color: white;
        }

    }
}

.copyright {
    color: grey;
    font-size: 17px;
    position: absolute;
    bottom: 30px;
    right: 40%;
}

.up {
    background-color: $primary_color;
    padding: 15px;
    border-radius: 50%;
    border: none;
    width: 60px;
    position: absolute;
    bottom: 20px;
    right: 20px;
    cursor: pointer;
}

a {
    text-decoration: none;
    color: white;

    i {
        font-size: 25px;
    }


}
</style>