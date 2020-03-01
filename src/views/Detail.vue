<template>
    <div class="detail">
        <div class="title">{{detail.title}}</div>
        <div class="summary">{{detail.summary}}</div>
        <div class="content">{{detail.content}}</div>
        <div class="create-time">{{detail.createTime}}</div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            detail: {
                id: 2,
                title: '编程必备基础知识 计算机组成原理+操作系统+计算机网络',
                img: 'https://img2.mukewang.com/szimg/5d1032ab08719e0906000338.jpg',
                summary: '介绍编程必备基础知识',
                content: '快速、系统补足必备的计算机系统知识，更快更有趣、更贴近实际工作，让你更快地学到满足实际工作需要的知识，为以后的工作打下良好的基础',
                createTime: '2019-08-10 10:20:20',
            }
        }
    }
}
</script>
<style scoped>
    .detail {
        padding: 20px;
        text-align: left;
    }
    .detail .title {
        font-size: 25px;
        padding-bottom: 20px;
    }
    .detail .summary {
        padding: 20px;
        background: #dcdcdc;
    }
    .detail .content {
        padding: 20px;
        text-indent: 2em;
        line-height: 200%;
    }
    .detail .create-time {
        color: #9c9c9c;
        text-align: right;
    }
</style>