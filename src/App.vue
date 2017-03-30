<template>
    <div id="app">
        <div class="header">
            <div class="menu" :class="{menu_sel: index == menu_sel_index}" v-for="(item, index) in menus"
                 @click="clickMenu(index)">{{item}}
            </div>

            <!-- 首页组件 -->
            <!-- 文章列表组件 -->
            <!-- 分类组件 -->
            <!-- 关于组件 -->

        </div>
    </div>
</template>

<script>
    export default {
        name: 'app',

        data () {
            return {
                menus: ["首页", "文章", "分类", "关于我"],
                menu_sel_index: 0,
            }
        },
        methods: {
            clickMenu: function (index) {
                this.menu_sel_index = index;
            }
        }
    }
</script>

<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        color: #2c3e50;
    }

    h1, h2 {
        font-weight: normal;
    }

    ul {
        list-style-type: none;
        padding: 0;
    }

    li {
        display: inline-block;
        margin: 0 10px;
    }

    a {
        color: #42b983;
    }

    .header {
        display: flex;
        width: 100%;
        height: 40px;
        align-items: center;
        border-bottom: 1px solid #eee;
    }

    .menu {
        display: flex;
        align-items: center;
        font-weight: bold;
        height: 34px;
        margin: 0 15px;
        border-bottom: 4px solid white;
        border-top: 2px solid white;
    }
    .menu:hover{
        color: #42b983;
    }

    /* 被选中的item */
    .menu_sel {
        border-bottom: 4px solid #42b983;
        color: #42b983;
    }
</style>
