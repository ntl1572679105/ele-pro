<template>
    <div>
        <el-container>
            <el-header class="header">
                <img src="../assets/element.svg" alt="" />
                <el-menu class="h-menu" default-active="1" mode="horizontal">
                    <el-menu-item index="1">指南 </el-menu-item>
                    <el-menu-item index="2">组件 </el-menu-item>
                    <el-menu-item index="3">主题 </el-menu-item>
                    <el-menu-item index="4">资源 </el-menu-item>
                </el-menu>
            </el-header>

            <el-container>
                <el-aside width="240px" class="aside">
                    <el-menu 
                    class="v-menu"
                    default-active="1"
                    active-text-color="#0062ff"
                    text-color="#666"
                    :router="true"
                    >
                        <el-menu-item index="/components/container" >
                            Container容器
                            <i class="el-icon-s-help"></i>
                        </el-menu-item>
                        <el-menu-item index="/components/table" >
                            Table表格
                            <i class="el-icon-s-unfold"></i>
                        </el-menu-item>
                        <el-menu-item index="/components/form" >
                            Form表单
                            <i class="el-icon-document"></i>
                        </el-menu-item>
                    </el-menu>
                </el-aside>

                <el-main> 
                    <!-- 二级路由占位符 -->
                    <router-view/>
                </el-main>
            </el-container>
        </el-container>
    </div>
</template>
<script>
export default {};
</script>

<style lang="scss" scoped>
.header {
    display: flex;
    align-items: center;
    border-bottom: 1px solid #e6e6e6;
    box-shadow: 0 4px 8px 0 rgb(0 44 102 / 5%);
}
.aside{
    box-shadow: 0 4px 8px 0 rgb(0 44 102 / 5%);
}
.h-menu {
    // border-bottom: none;
    margin-left: 50px;
}
.v-menu{
    border-right: none;
    text-align:left;
    margin-top: 10px;
    height: calc(100vh - 70px);
}
.v-menu .el-menu-item.is-active{
    background-color: #ebf3ff;
    border-right: 2px solid #0062ff;
}
.v-menu .el-menu-item i{
    float: right;
    height: 50px;
    line-height: 50px;
}
// .v-menu .el-menu-item {
//     router:true,
// }
</style>