<template>
 <div id="app">
    <!--iview Menu MenuItem SubMenu-->
    <!-- 递归组件 树结构 菜单-->
    <Menu>
        <template v-for="menu in menuList">
            <MenuItem
                :key="menu.title"
                v-if="!menu.children"
            >
                {{menu.title}}
            </MenuItem>
            <ReSubMenu 
                v-else
                :key="menu.title"
                :data="menu"
            ></ReSubMenu>
        </template>
    </Menu>
 </div>
</template>
<script>
import Menu from './Menu';
import MenuItem from './MenuItem';
import SubMenu from './SubMenu';
import ReSubMenu from './ReSubMenu';
// 使用组件 3步骤 定义组件 引用组件 注册组件
export default {
    data(){
        return {
            msg: 'hello',
            menuList: [{
                title: '菜单1',
                children: [{
                    title: '菜单1-1',
                    children: [{
                        title:'菜单1-1-1'
                    },{
                        title:'菜单1-1-2'
                    },{
                        title:'菜单1-1-3'
                    }]
                },{
                    title: '菜单1-2',
                     children: [{
                        title:'菜单1-2-1'
                    },{
                        title:'菜单1-2-2'
                    },{
                        title:'菜单1-2-3'
                    }]
                },{
                    title: '菜单1-3',
                     children: [{
                        title:'菜单1-3-1'
                    },{
                        title:'菜单1-3-2'
                    },{
                        title:'菜单1-3-3',
                        children: [{
                            title:'菜单1-3-3-1'
                        },{
                            title:'菜单1-3-3-2'
                        },{
                            title:'菜单1-3-3-3'
                        }]
                    }]
                }]
            },{
                title: '菜单2'
            },{
                title: '菜单3'
            }]
        };
    },
    components: {
        Menu,
        MenuItem,
        SubMenu,
        ReSubMenu
    }
}
</script>
<style>
#app{
    color: red;
}
</style>