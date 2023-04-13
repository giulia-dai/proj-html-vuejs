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
            ]
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



    </div>
</template>

<style scoped lang="scss">
@use '../styles/generals.scss' as *;

.contain {
    min-height: 250px;
    background-color: black;
    padding: 15px;
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
</style>