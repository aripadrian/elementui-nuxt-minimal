<template>
  <el-container style="min-height: 100vh">
    <el-aside width="260px" style="min-height: 100vh">
      <el-menu
        style="min-height: 100vh"
        default-active="2"
        class="el-menu-vertical-demo"
        :collapse="isCollapse"
        @open="handleOpen"
        @close="handleClose"
      >
        <!-- <el-submenu index="1">
          <template slot="title">
            <i class="el-icon-location"></i>
            <span slot="title">Navigator One</span>
          </template>
        </el-submenu> -->
        <el-menu-item index="2">
          <i class="el-icon-s-home"></i>
          <span slot="title">Dashboard</span>
        </el-menu-item>

        <el-menu-item index="4">
          <i class="el-icon-setting"></i>
          <span slot="title">Navigator Four</span>
        </el-menu-item>
      </el-menu>
    </el-aside>

    <el-container>
      <el-header style="text-align: right; font-size: 12px">
        <el-dropdown>
          <i class="el-icon-setting" style="margin-right: 15px"></i>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>View</el-dropdown-item>
            <el-dropdown-item>Add</el-dropdown-item>
            <el-dropdown-item>Delete</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
        <span>Tom</span>
      </el-header>

      <el-main>
        <nuxt />
      </el-main>
    </el-container>
  </el-container>
</template>

<script>
export default {
  name: 'DefaultLayout',
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap');
html,
body {
  font-family: 'Roboto', sans-serif;
}

/* width */
::-webkit-scrollbar {
  width: 10px;
}

/* Track */
::-webkit-scrollbar-track {
  background: #f1f1f1;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: #888;
  border-radius: 99px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #555;
}
</style>
