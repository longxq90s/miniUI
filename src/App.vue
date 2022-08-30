<template>
  <div id="app">
    <div class="demo-button">
      <div class="c-row">
        <or-button >默认按钮</or-button>
        <or-button type="primary">主要按钮</or-button>
        <or-button type="success">成功按钮</or-button>
        <or-button type="info">信息按钮</or-button>
        <or-button type="warning">警告按钮</or-button>
        <or-button type="danger">危险按钮</or-button>
      </div>
      <div class="c-row">
        <or-button plain>朴素按钮</or-button>
        <or-button type="primary" plain>主要按钮</or-button>
        <or-button type="success" plain>成功按钮</or-button>
        <or-button type="info" plain >信息按钮</or-button>
        <or-button type="warning" plain>警告按钮</or-button>
        <or-button type="danger" plain>危险按钮</or-button>
      </div>
      <div class="c-row">
        <or-button round>朴素按钮</or-button>
        <or-button type="primary" round>主要按钮</or-button>
        <or-button type="success" round>成功按钮</or-button>
        <or-button type="info" round >信息按钮</or-button>
        <or-button type="warning" round>警告按钮</or-button>
        <or-button type="danger" round>危险按钮</or-button>
      </div>
      <div class="c-row">
        <or-button circle icon="or-icon-house"></or-button>
        <or-button type="primary" circle icon="or-icon-search"></or-button>
        <or-button type="success" circle icon="or-icon-success"></or-button>
        <or-button type="info" circle icon="or-icon-info"></or-button>
        <or-button type="warning" circle icon="or-icon-warning"></or-button>
        <or-button type="danger" circle icon="or-icon-error"></or-button>
      </div>
      <div class="c-row">
        <or-button @click="testFun" disable loading>默认按钮</or-button>
        <or-button type="primary"disable>主要按钮</or-button>
        <or-button type="success"disable>成功按钮</or-button>
        <or-button type="info"disable>信息按钮</or-button>
        <or-button type="warning"disable>警告按钮</or-button>
        <or-button type="danger"disable>危险按钮</or-button>
      </div>
      <div class="c-row">
        <or-button type="text">文本按钮</or-button>
        <or-button @click="testFun" type="text" disable>文本按钮</or-button>
      </div>
      <div class="c-row">
        <or-button-group>
          <or-button  type="primary">上一页</or-button>
          <or-button type="primary">下一页</or-button>
        </or-button-group>
      </div>
      <div class="c-row">
        <or-button >默认按钮</or-button>
        <or-button size="medium">中等尺寸</or-button>
        <or-button size="small">小尺寸</or-button>
        <or-button size="mini">mini</or-button>
      </div>
      <div class="c-row">
        <or-button round>默认按钮</or-button>
        <or-button size="medium" round>中等尺寸</or-button>
        <or-button size="small" round>小尺寸</or-button>
        <or-button round size="mini">mini</or-button>
      </div>
      <div class="c-row">
        <or-button round>默认按钮</or-button>
        <or-button native-type="submit" size="medium" round>submit</or-button>
        <or-button native-type="reset" size="small" round>重置按钮</or-button>
        <or-button autofocus size="small" round>重置按钮</or-button>
      </div>
    </div>
  </div>
</template>

<script>

import orButton from './components/button/button.vue'
import orButtonGroup from './components/button/buttonGroup'

export default {
  name: "app",
  components: {
    orButton,
    orButtonGroup
  },
  methods:{
    testFun(){
      alert('123')
    }
  }
}
</script>
<style lang="scss">
#app{
  font-family: 'Avenir','Helvetica','Arial';
  //text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.demo-button > .c-row{
  margin-top: 20px;
}
.demo-button > .or-button + .or-button {
  margin-left:10px ;
}
</style>

