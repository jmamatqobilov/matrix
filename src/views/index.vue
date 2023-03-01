<template>
    <Header />
    <div class="container">
        <div class="tabbar-container">
            <div class="">
                <div class="">
                    <img :src="require('../assets/title.svg')" />
                </div>
            </div>
            <div class="tab-columns">
                <v-row class="">
                    <v-col cols="12" sm="4" class="tab-line d-flex justify-center" v-for="(category, index) in categories"
                        :key="index" @click="categoryIndex = category.title">
                        <router-link :to="category.to">
                            <a :class="categoryIndex === category.title ? ' active' : ''">
                                {{ category.title }}
                            </a>
                        </router-link>
                    </v-col>
                </v-row>
                <div class="tabbar-liner">

                </div>

            </div>
        </div>
    </div>
    <router-view />
</template>
  
<script>


// Components

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
li {
    list-style: none;
    text-decoration: none;
}

a {
    text-decoration: none;
    list-style: none;
}

.tab-line a{
    color: red;
}
.tab-line a{
    color:#B7C2BF;
    font-size: 16px;
    font-weight: 600;
    line-height: 24px;
    position: relative;
}
.tab-line:nth-child(1) a.active{                
    position: relative;
    color: #229A87;
}
.tab-line:nth-child(1) a.active::before{
    content: '';
    position: absolute;
    width: 100%;
    height: 4px;
    bottom:0;
    right: 0;
    background: rgb(16, 18, 16);
    
}
.tab-line:nth-child(2) a.active{
    position: relative;
    color: #229A87;
}
.tab-line:nth-child(2) a.active::before{
    content: '';
    position: absolute;
    width: 100%;
    height: 4px;
    bottom:0;
    right: 0;
    background: rgb(16, 18, 16);
    
}
.tab-line:nth-child(3) a.active{
    position: relative;
    color: #229A87;
}
.tab-line:nth-child(3) a.active::before{
    content: '';
    position: absolute;
    width: 100%;
    height: 4px;
    bottom:0;
    right: 0;
    background: rgb(16, 18, 16);
    
}









.tabbar-container {
    padding-top: 40px;
}

.tab-columns {
    justify-content: center;
}

.tabbar-liner {
    margin-top: 16px;
    width: 100%;
    height: 1px;
    background: #36A593;
}
</style>
  