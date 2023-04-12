<script>
export default {
    name: "AppNav",
    data() {
        return {
            items: [
                'Home',
                'Pages',
                'Courses',
                'Features',
                'Blog',
                'Shop'
            ]
        }
    }
}
</script>
<template>
    <h1>APPNAV</h1>
    <nav>
        <div class="container">
            <div class="wrapper">
                <img class="wrapped-img" src="../assets/images/dark-logo.png" alt="logo">
            </div>

            <div>
                <ul class="menu">
                    <li v-for="item in items">{{ item }} <i class="fa-solid fa-chevron-down"></i></li>
                </ul>

            </div>

            <div class="change-lang">
                <div class="flag-wrapper">
                    <img src="../assets/images/en.png" alt="flag">
                </div>
                <select name="language" id="language">
                    <option>ENGLISH</option>
                    <option>GERMAN</option>
                    <option>FRENCH</option>

                </select>

                <div class="user">
                    <i class="fa-regular fa-circle-user"></i>
                </div>
            </div>



            <form>
                <input class="searchbar" type="text" placeholder="Search">
            </form>
            <i class="fa-solid fa-magnifying-glass"></i>
        </div>
    </nav>
</template>


<style scoped lang="scss">
.wrapper {
    width: 15%;

    .wrapped-img {
        width: 100%;
    }
}

.menu {
    display: flex;
    list-style: none;
    padding: 10px;

    li {
        margin: 1rem;
        cursor: pointer;
        vertical-align: middle;

        &:hover {
            text-decoration: underline;
        }

        i {
            font-size: 11px;
        }
    }
}

.change-lang {
    display: flex;
    align-items: center;
}

#language {
    border: none;
    background: none;
    margin-left: 0.4rem;
}

.user {
    font-size: 18px;
    padding: 10px;
    cursor: pointer;
}

.searchbar {
    border: none;
    padding: 10px;
}
</style>