<template>
  <div class="SBY_home">
    <img style="width: 100%;" src="http://buy.sbyun.com/skins2/images/BANNER-4.jpg">

    <div class="TextCenter OneBlock">
      <Row type="flex" justify="space-around" class="code-row-bg PaddingLR_20" :gutter="16">
        <Col :xs="24" :sm="12" :md="{span: 6, offset: 3}" :lg="{span: 6, offset: 3}" class="TextCenter marginB_20">
          <Card class="IndividualCard">
            <p slot="title" style="text-align: left;color: #fff;">
                <Icon type="android-contact"></Icon>
                个人缴纳社保<span style="font-size: 6px;margin-left: 10px;">服务费</span>
            </p>
            <h5 class="marginTB_10"><span class="BigSize">¥40</span>/人.月</h5>
            <Button class="marginTB_10" type="warning" @click="ToSBY(0)">立即参保</Button>
          </Card>
        </Col>

        <Col :xs="24" :sm="12" :md="{span: 6, offset: 3}" :lg="{span: 6, offset: 3}" class="TextCenter">
          <Card class="EnterpriseCard">
            <p slot="title" style="text-align: left;color: #fff;">
                <Icon type="android-contacts"></Icon>
                企业缴纳社保<span style="font-size: 6px;margin-left: 10px;">按员工数收费</span>
            </p>
            <h5 class="marginTB_10"><span class="BigSize">¥20</span>/人.月</h5>
            <Button class="marginTB_10" type="warning" @click="ToSBY(1)">立即参保</Button>
          </Card>
        </Col>
        <div style="clear: both;"></div>
      </Row>
    </div>

    <div class="TextCenter OneBlock">
      <Row type="flex" justify="space-around" class="code-row-bg Bg_lightGreen">
        <Col class="marginT_20" :xs="12" :sm="6" :md="6" :lg="6" v-for="(Block,Idx) in BlockInfo">
          <h2 class="ColorGreen">{{Block.title_b}}</h2>
          <h5 class="ColorGreen">{{Block.title_s}}</h5>
          <p class="marginTB_10"><Icon :type="Block.icon"></Icon>{{Block.content}}</p>
        </Col>
        <div style="clear: both;"></div>
      </Row>
    </div>

    <div class="TextCenter OneBlock">
      <h2 class="marginTB_20">无论您为什么要缴纳社保，我们帮您搞定</h2>
      <Row type="flex" justify="space-around" class="code-row-bg">
        <Col class="marginT_20" :xs="12" :sm="6" :md="6" :lg="6" v-for="(Reason,Idx) in ReasonInfo">
          <img style="width: 50px;" :src="Reason.img">
          <h5 class="marginTB_10">{{Reason.title}}</h5>
        </Col>
        <div style="clear: both;"></div>
      </Row>
      <h5 class="marginTB_20"><Icon type="chatboxes" style="margin-right: 5px;"></Icon>有更多原因需要缴纳社保，我们帮您解决</h5>
    </div>

    <div class="TextCenter OneBlock">
      <h2 class="marginTB_20">一分钟轻松注册，即可开启社保服务</h2>
      <Row type="flex" justify="space-around" class="code-row-bg">
        <Col class="marginT_20" :xs="12" :sm="4" :md="4" :lg="4" v-for="(Process,Idx) in ProcessInfo">
          <img style="width: 50px;" :src="Process.img">
          <h5 class="marginTB_10">{{Process.title}}</h5>
        </Col>
        <div style="clear: both;"></div>
      </Row>
    </div>
    
    
     
  </div>
</template>
<script>
// import Carousel from '../components/Carousel/Carousel'
  export default{
    data: function () {
      return {
        BlockInfo:[
          {'title_b':'正规资质','title_s':'不经手第三方','content':'查阅劳动派遣许可证','link':'','icon':'search'},
          {'title_b':'24H在线','title_s':'足不出户缴纳','content':'申请微信缴纳','link':'','icon':'chatbubble'},
          {'title_b':'按月操作','title_s':'跨城市联网','content':'了解开通城市','link':'','icon':'ios-world-outline'},
          {'title_b':'价格透明','title_s':'不含隐形收费','content':'查看收费标准','link':'','icon':'social-usd'}
        ],
        ReasonInfo:[
          {'title':'领养老金','img':'https://surveyanyplace.com/wp-content/uploads/10-1-120x120.png'},
          {'title':'买房资格','img':'static/img/SBY/icon/SBY_Home_icon_mf.png'},
          {'title':'孩子入学','img':'static/img/SBY/icon/SBY_Home_icon_rx.png'},
          {'title':'医疗保证','img':'static/img/SBY/icon/SBY_Home_icon_yl.png'},
          {'title':'买车需求','img':'static/img/SBY/icon/SBY_Home_icon_mc.png'},
          {'title':'积分办理','img':'static/img/SBY/icon/SBY_Home_icon_jf.png'},
          {'title':'异地高考','img':'static/img/SBY/icon/SBY_Home_icon_gk.png'},
          {'title':'出国签证','img':'static/img/SBY/icon/SBY_Home_icon_qz.png'}
        ],
        ProcessInfo:[
          {'title':'注册登录','img':'static/img/SBY/icon/SBY_Home_icon_zc.svg'},
          {'title':'选择付费周期','img':'static/img/SBY/icon/SBY_Home_icon_sj.svg'},
          {'title':'缴纳参保费用','img':'static/img/SBY/icon/SBY_Home_icon_jn.svg'},
          {'title':'审核资料/参保','img':'static/img/SBY/icon/SBY_Home_icon_sh.svg'},
          {'title':'参保成功','img':'static/img/SBY/icon/SBY_Home_icon_cg.svg'},
          {'title':'短信提醒','img':'static/img/SBY/icon/SBY_Home_icon_dx.svg'},
        ]
      }
    },
    mounted: function () {
      
    },
    created: function () {
      
    },
    computed: {
      open:{
          get: function () {
            return this.$store.state.open
          },
          set: function (newValue) {
            this.$store.state.open = newValue
          }
      }
      
    },
    watch: {
      
    },
    components: {
      

    },
    methods: {
      ChangeTab_Product(Menu){
        this.Cur_Product = Menu
      },
      ToSBY(Kind){
        switch(Kind){
          case 0:
          window.open('http://220.248.107.62:8089/ztnetsby/#/Individual')
          break
          case 1:
          window.open('http://220.248.107.62:8089/ztnetsby/#/Enterprise')
          break
          default:
          window.open('http://220.248.107.62:8089/ztnetsby')

        }
        
      }
     

    }
  }
</script>
<style lang="scss">
.SBY_home{
  .IndividualCard{
    .ivu-card-head{
      background-color: #ff7a78;
    }
  }
  .EnterpriseCard{
    .ivu-card-head{
      background-color: #37ba7e;
    }
  }
  .BigSize{
    font-size: 35px;
    color: red;
  }
  .ColorGreen{
    color: #37ba7e;
  }
  .Bg_lightGreen{
    background-color: #e5f0e7;
  }
  
  img{
    max-width: 100%;
  }

}
</style>
