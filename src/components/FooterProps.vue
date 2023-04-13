<script>
export default {
    name: 'FooterProps',
    data() {
        return {

        };
    },
    props: {
        big_title: String,
        country: String,
        phone: String,
        mail: String
    }
}
</script>

<template>
    <div>
        <h3 class="white">{{ big_title }}</h3>
        <div class="txt">
            <div>{{ country }}</div>
            <div>{{ phone }}</div>
            <div>{{ mail }}</div>
        </div>

    </div>
</template>

<style scoped lang="scss">
.white {
    color: white;
}

.txt {
    color: #9B9B9C;
    line-height: 30px;
}
</style>