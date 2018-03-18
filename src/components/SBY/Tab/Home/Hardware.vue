<template>
  <div class="Hardware">
  <div class="BlockOuter">
     <div class="OneBlock TextLeft">
            <h2 class="marginTB_20">智能硬件产品</h2>
            <p>物联网 (IoT)始于“物”（即设备）。构建您的设备（从添加传感器到创建智能设备），才能启动您的 IoT 解决方案。我们提供如下产品</p>
            <Row type="flex"  justify="center"  class="code-row-bg marginTB_40":gutter="16">
                <Col class="marginB_20" :xs="12" :sm="8" :md="4" :lg="4" v-for="(Hardware,Idx) in HardwareList">
                    <div class="SingleImg">
                        <img style="width: 120px; height: 120px;" :src="Hardware.img">
                        <h5>{{Hardware.name}}</h5>
                    </div>
                </Col>
                <div style="clear: both;"></div>
            </Row>
        </div>

        <div class="OneBlock">
            <h2 class="marginTB_20 TextLeft">ODM</h2>
            <h2 class="TextLeft">为你的传统电器，插上智能的“翅膀”</h2>
            <div class="TextCenter SingleImg">
                <img src="static/img/Icon/SmartHox_Products_icon13.png">
            </div>
        </div>
        </div>
  </div>
</template>
<script>
  export default{
    data: function () {
      return {
        HardwareList:[
            {'name':'智能网关','img':'static/img/Icon/SmartHox_Products_icon7.png'},
            {'name':'智能电箱','img':'static/img/Icon/SmartHox_Products_icon8.png'},
            {'name':'协议转换器','img':'static/img/Icon/SmartHox_Products_icon9.png'},
            {'name':'无源开关','img':'static/img/Icon/SmartHox_Products_icon10.png'},
            {'name':'随意智能音箱','img':'static/img/Icon/SmartHox_Products_icon11.png'},
            {'name':'传感设备','img':'static/img/Icon/SmartHox_Products_icon12.png'}
        ]
      }
    },
    mounted: function () {
      
    },
    created: function () {
      
    },
    computed: {
    },
    watch: {
      
    },
    components: {
    },
    methods: {
     

    }
  }
</script>
<style lang="scss">
.Hardware{
  .BlockOuter{
      padding: 20px 20px;
      .mu-tabs{
          background-color: #fff !important;
      }
      .mu-tab-text{
          color: #000;
      }
      .mu-icon{
          color: #000;
      }
  }

}
</style>
