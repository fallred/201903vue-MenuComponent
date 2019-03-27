npm install @vue/cli -g .vue
npm install -g @vue/cli-service-global
vue serve App.vue

<Menu>
    <MenuItem>菜单1</MenuItem>
    <MenuItem>菜单2</MenuItem>
    <MenuItem>菜单3</MenuItem>
    <SubMenu>
        <template #title>
            菜单4
        </template>
        <MenuItem>菜单4-1</MenuItem>
        <MenuItem>菜单4-2</MenuItem>
        <SubMenu>
            <template #title>
                菜单4-3
            </template>
            <MenuItem>菜单4-3-1</MenuItem>
            <MenuItem>菜单4-3-2</MenuItem>
            <SubMenu>
                <template #title>
                    菜单4-3-3
                </template>
                <MenuItem>菜单4-3-3-1</MenuItem>
                <MenuItem>菜单4-3-3-2</MenuItem>
            </SubMenu>
        </SubMenu>
    </SubMenu>
</Menu>