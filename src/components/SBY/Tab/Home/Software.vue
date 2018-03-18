<template>
  <div class="Iot">
    <div class="TextLeft BlockOuter">
      <h5 class="TextCenter marginB_10">殡葬管理云平台</h5>
      <p class="TextCenter marginB_10">助力民政殡葬信息化建设</p>
      <Row type="flex" justify="" class="code-row-bg marginT_20">
        <Col :xs="24" :sm="12" :md="6" :lg="6" v-for="(Product,Idx) in ProductList">
          {{Product.name}}
        </Col>
      </Row>
    </div>
    <div class="TextCenter BlockOuter">
      <h5 class="marginB_10">软件定制</h5>
      <p class="marginB_10">Ztnet&Btzoon可根据企业的需求，定制更贴合您的业务，让系统更高效更便捷</p>

      <Row type="flex" justify="center" class="code-row-bg marginT_40">
        <Col class="TextCenter marginB_10" :xs="24" :sm="6" :md="6" :lg="6" v-for="(Customization,Idx) in Customization">
          <Button :class="{'Green': Idx == 0,'Blue': Idx == 1,'Orange': Idx == 2,'Puple': Idx == 3}" style="color: #fff;" type="text" shape="circle">{{Customization.name}}</Button>
        </Col>
      </Row>

    </div>
  </div>
</template>
<script>
  export default{
    data: function () {
      return {
        ProductList:[
          {'name':'数字化殡仪业务管理系统','link':''},
          {'name':'数字化陵园业务管理系统','link':''},
          {'name':'数字化殡仪IC卡管理系统','link':''},
          {'name':'数字化陵园工程管理系统','link':''},
          {'name':'数字化骨灰寄存管理系统','link':''},
          {'name':'数字化陵园档案管理系统','link':''},
          {'name':'数字化殡仪协同OA系统','link':''},
          {'name':'陵园业务移动应用APP','link':''},
          {'name':'数字化档案管理系统','link':''},
          {'name':'网站信息发布系统','link':''},
          {'name':'殡仪业务移动应用APP','link':''},
          {'name':'统计分析及决策系统','link':''},
          {'name':'电子商务平台（O2O)','link':''},
          {'name':'殡葬管理绩效考核系统','link':''},
          {'name':'场馆预约管理系统','link':''},
        ],
        Customization:[
          {'name':'行业软件定制','link':''},
          {'name':'APP应用开发','link':''},
          {'name':'小程序定制','link':''},
          {'name':'金蝶二次开发','link':''}
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
      .Green{
        background-color: #37ba7e;
      }
      .Blue{
        background-color: #16a6e9;
      }
      .Orange{
        background-color: #fb9a00;
      }
      .Puple{
        background-color: #b448ff;
      }
  }

}
</style>
