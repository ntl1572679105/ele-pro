<template>
    <div>
        <!-- 水平导航 -->
        <el-menu :default-active="active" mode="horizontal">
            <el-menu-item index="1">首页</el-menu-item>
            <el-menu-item index="2">朋友圈</el-menu-item>
            <el-submenu index="3">
                <template slot="title">主题</template>
                <el-menu-item index="3-1">中国红</el-menu-item>
                <el-menu-item index="3-2">深海蓝</el-menu-item>
                <el-menu-item index="3-3">曜石黑</el-menu-item>
            </el-submenu>
            <el-menu-item index="4">帮助</el-menu-item>
        </el-menu>

        <!-- 垂直导航 -->
        <el-menu 
        class="my-menu"
        style="width: 220px" 
        :default-active="active"
        text-color="#0000ff" 
        active-text-color="#ff0000">
            <el-menu-item index="1">首页</el-menu-item>
            <el-menu-item index="2">朋友圈</el-menu-item>
            <el-submenu index="3">
                <template slot="title">主题</template>
                <el-menu-item index="3-1">中国红</el-menu-item>
                <el-menu-item index="3-2">深海蓝</el-menu-item>
                <el-menu-item index="3-3">曜石黑</el-menu-item>
            </el-submenu>
            <el-menu-item index="4">帮助</el-menu-item>
        </el-menu>

    </div>
</template>

<script>
export default {
    data() {
        return {
            active: '1'
        }
    },
}
</script>

<style lang="scss" scoped>

.my-menu,
.el-menu-item {
    height: 48px;
    line-height: 48px;
}
</style>

<style>
.el-submenu__title {
    height: 48px;
    line-height: 48px;
}
</style>