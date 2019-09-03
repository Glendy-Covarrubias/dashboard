<template>
  <a-layout id="components-layout-demo-side" style="min-height: 100vh">

    <a-layout-sider
      collapsible
      v-model="collapsed"
      @click="titleShow"
    >
      <!-- Encabezado del menu -->
      <div class="logo"><label for="capacitacion" >{{titleBar}}</label></div>

      <!-- Menu -->
      <a-menu theme="dark" :defaultSelectedKeys="['1']" mode="inline">  

        <a-sub-menu key="sub1">
          <span slot="title"><a-icon type="star" theme="filled"/><span>PHP</span></span>
          <a-menu-item key="3">Tom</a-menu-item>
          <a-menu-item key="4">Bill</a-menu-item>
          <a-menu-item key="5">Alex</a-menu-item>
        </a-sub-menu>

        <a-sub-menu key="sub2">
          <span slot="title"><a-icon type="like" theme="filled"/><span>VUE</span></span>
          <a-menu-item key="6">Team 1</a-menu-item>
          <a-menu-item key="8">Team 2</a-menu-item>
        </a-sub-menu>

        <a-menu-item key="9">
          <a-icon type="android" theme="filled"/>
          <span>ANDROID</span>
        </a-menu-item>

        <a-sub-menu key="sub3">
          <span slot="title"><a-icon type="smile" theme="filled"/><span>PYTHON</span></span>
          <a-menu-item key="3">Django</a-menu-item>
          <a-menu-item key="4">Bill</a-menu-item>
          <a-menu-item key="5">Alex</a-menu-item>
        </a-sub-menu>

      </a-menu>
      
    </a-layout-sider>

    <a-layout>
      <a-layout-header style="background: #fff; padding: 0"> 
        <h1 class="title">{{titleSection}}</h1>
      </a-layout-header>


      <a-layout-content style="margin: 0 16px">
        <br>
        <!-- <a-breadcrumb style="margin: 16px 0">
          <a-breadcrumb-item>Avance</a-breadcrumb-item>
          <a-breadcrumb-item>Ejemplo</a-breadcrumb-item>
          <a-breadcrumb-item>Resultado</a-breadcrumb-item>
        </a-breadcrumb> -->
        <div :style="{ padding: '24px', background: '#fff', minHeight: '360px' }">
          <tab-component />
        </div>
      </a-layout-content>

      <!-- footer -->
      <a-layout-footer style="text-align: center">
        Ant Design ©2018 Created by Ant UED
      </a-layout-footer>

    </a-layout>

  </a-layout>
</template>
<script>
import TabComponent from "./TabComponent.vue"
export default {
  components : {
    TabComponent
  },
  data() {
    return {
      collapsed     : false,
      titleBar      : "Capacitación",
      titleSection  : "Mi Dashboard </>"
    }
  },
  mounted(){
    // invocar los métodos
    // this.getSession();
    // console.log(this.collapsed);
  },
  methods : {
    titleShow(){ //Validamos como se encuentra el menu abierto o cerrado
      this.collapsed == true ? this.titleBar = "C" : this.titleBar = "Capacitación";
    }
  }
}
</script>

<style>
#components-layout-demo-side .logo {
  height: 32px;
  /* background: rgba(255,255,255,.2); */
  margin: 16px;
  text-align: center;
  color: white;
  font-size: 1em;
  font-weight: bold;
  background-color: #2c1244;
  padding-top: 0.5em;
}

.title{
  text-align: center;
}
</style>
