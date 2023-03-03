<template>
    <Header />
    <v-container>
        <div class="tabbar-container">
            <div class="">
                <div class="">
                    <img :src="require('../assets/title.svg')" />
                </div>
            </div>
            <div class="tab-columns">
                <v-row class="">
                    <v-col cols="12" sm="4" class="tab-line d-flex justify-center" v-for="(category, index) in categories"
                        :key="index" @click="categoryIndex = (index+1)">
                        <router-link :to="category.to">
                            <a :class="categoryIndex === category.title ? ' active' : ''">
                                {{ category.title }}
                            </a>
                        </router-link>
                    </v-col>
                </v-row>
                <div class="tabbar-liner">
                    <div :style="{ width: '33.33333333%', transform: 'translateX(' + `${(categoryIndex - 1) * 100}%` + ')' }"
                        class="inner-line">
                    </div>
                </div>
            </div>
        </div>
    </v-container>
    <div style="margin-top: 40px;margin-bottom: 20px;"></div>
    <router-view />
</template>
  
<script>
import Header from '@/components/Header.vue';
export default {
    name: 'Index',
    components: {
        Header
    },

    data() {
        return {
            tab: null,
            categories: [
                {
                    to: "/subjects",
                    title: "Subjects"
                },
                {
                    to: "/motivation",
                    title: "Motivation"
                },
                {
                    to: "/training",
                    title: "Training"
                }
            ],
            categoryIndex: 1
        }
    },
};
</script>

<style scoped>
.tabbar-liner {
    margin-top: 15px;
    background-color: #cad8d6;
    height: 1px;
    display: flex;
    align-items: center;
}
.inner-line {
    transition: all .3s ease;
    height: 4px;
    border-radius: 10px;
    background-color: #36A593;
}


li {
    list-style: none;
    text-decoration: none;
}

a {
    text-decoration: none;
    list-style: none;
}

.tab-line a {
    color: red;
}

.tab-line a {
    color: #B7C2BF;
    font-size: 16px;
    font-weight: 600;
    line-height: 24px;
    position: relative;
}

.tab-line:nth-child(1) a.active {
    position: relative;
    color: #229A87;
}

.tab-line:nth-child(1) a.active::before {
    content: '';
    position: absolute;
    width: 100%;
    height: 4px;
    bottom: 0;
    right: 0;
    background: rgb(16, 18, 16);

}

.tab-line:nth-child(2) a.active {
    position: relative;
    color: #229A87;
}

.tab-line:nth-child(2) a.active::before {
    content: '';
    position: absolute;
    width: 100%;
    height: 4px;
    bottom: 0;
    right: 0;
    background: rgb(16, 18, 16);

}

.tab-line:nth-child(3) a.active {
    position: relative;
    color: #229A87;
}

.tab-line:nth-child(3) a.active::before {
    content: '';
    position: absolute;
    width: 100%;
    height: 4px;
    bottom: 0;
    right: 0;
    background: rgb(16, 18, 16);

}


.tabbar-container {
    padding-top: 40px;
}

.tab-columns {
    justify-content: center;
}

</style>
  