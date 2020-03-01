<template>
    <div>
        <van-list
        v-model="loading"
        :finished="finished"
        finished-text="没有更多了"
        @load="onLoad"
        >
        <van-cell v-for="item in list" :key="item.id" @click="handleClick(item.id)">
            <div class="list">
                <div class="left">
                    <img :src="item.img" alt="">
                </div>
                <div class="right">
                    <div class="title">{{item.title}}</div>
                    <div class="create-time">{{item.createTime}}</div>
                </div>
            </div>
        </van-cell>
        </van-list>
    </div>
</template>
<script>
import { List, Cell } from 'vant';
export default {
    components: {
        [List.name]: List,
        [Cell.name]: Cell,
    },
    data() {
        return {
            loading: false,
            finished: false,
            list: []
        }
    },
    methods: {
        onLoad() {
            setTimeout(() => {
                this.loading = false,
                this.finished = true,
                this.list = [
                    {
                        id: 1,
                        title: '编程必备基础知识 计算机组成原理+操作系统+计算机网络',
                        img: 'https://img2.mukewang.com/szimg/5d1032ab08719e0906000338.jpg',
                        summary: '介绍编程必备基础知识',
                        content: '快速、系统补足必备的计算机系统知识，更快更有趣、更贴近实际工作，让你更快地学到满足实际工作需要的知识，为以后的工作打下良好的基础',
                        createTime: '2019-08-10 10:20:20',
                    },
                    {
                        id: 2,
                        title: '编程必备基础知识 计算机组成原理+操作系统+计算机网络',
                        img: 'https://img2.mukewang.com/szimg/5d1032ab08719e0906000338.jpg',
                        summary: '介绍编程必备基础知识',
                        content: '快速、系统补足必备的计算机系统知识，更快更有趣、更贴近实际工作，让你更快地学到满足实际工作需要的知识，为以后的工作打下良好的基础',
                        createTime: '2019-08-10 10:20:20',
                    },                    
                ]
            }, 1000)
        },
        handleClick(id) {
            this.$router.push({
                path: '/detail',
                query: {
                    id
                }
            })
        }
    }
}
</script>
<style scoped>
    .list {
        display: flex;
        flex-direction: row;
    }
    .list .left img {
        width: 150px;
        height: 100px;
        border-radius: 10px;
    }
    .list .right {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        margin-left: 15px;
    }
    .list .right .title {
        font-size: 18px;
    }
    .list .right .create-time {
        font-size: 12px;
        color: #9e9e9e;
    }
</style>