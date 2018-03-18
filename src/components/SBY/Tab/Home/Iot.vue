<template>
  <div class="Iot">
    <div class="BlockOuter">
      <h5 class="TextLeft">物联网一站式纵向服务</h5>
      <p class="TextLeft">Smart Hox 作为物联网行业极具创新能力的IoT云平台，为企业提供进入物联网必需的设备接入、设备控制、数据分析、供应链资源一站式服务，助力企业智造转型，并为其在物联网时代打造新商业模式。</p>
      <Row  type="flex"  justify="center"  class="code-row-bg marginTB_40 TextCenter" :gutter="16">

          <Col class="marginB_10" :xs="24" :sm="12" :md="6"  :lg="6" v-for="(Block,Idx) in BlockInfo">
            <img class="marginB_20" :src="Block.img"/>
            <h5 class="Bold TextLeft marginTB_20">{{Block.title}}</h5>
            <p class="TextLeft">{{Block.content}}</p>
          </Col>
      </Row>
    </div>
  </div>
</template>
<script>
  export default{
    data: function () {
      return {
        BlockInfo:[
          {'title':'构建设备','content':'物联网 (IoT)始于“物”（即设备）。构建您的设备（从添加传感器到创建智能设备），才能启动您的 IoT 解决方案。','img':'/static/img/Icon/Home/SmartHox_Home_icon1.png'},
          {'title':'控制您的设备','content':'部署控制、监控和管理您的设备的 IoT 解决方案，从而允许您捕获实时数据。','img':'/static/img/Icon/Home/SmartHox_Home_icon14.png'},
          {'title':'分析数据','content':'利用您收集的数据并应用高级分析以揭示新业务见解。','img':'/static/img/Icon/Home/SmartHox_Home_icon2.png'},
          {'title':'针对见解采取措施','content':'通过功能强大的应用程序将见解转变为行动，从而创造新的收入和业务机会。','img':'/static/img/Icon/Home/SmartHox_Home_icon13.png'},
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
.Iot{
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
  img{
        max-width: 100% !important;
  }

}
</style>
