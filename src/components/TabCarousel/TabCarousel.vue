<template>
  <div class="TabCarousel">
       <div class="section carousel" style="margin-top:-25px;"> 
         <div class="transitionValue" transitionvalue="10" style="transition: none 0s ease 0s ;"></div> 
         <div class="transitionOffOn" transitionoffon="" style="transition: none 0s ease 0s ;"></div> 
   <!--Carousel module starts here--> 
   <div class="section full-width" style="transition: none 0s ease 0s ;"> 
    <div class="container-fluid" style="transition: none 0s ease 0s ;"> 
     <div class="row"> 
      <div class="col-md-12"> 
       <div class="customerBanner"> 
        <div class="owl-container"> 
         <div id="customerSlider" class="owl-carousel owl-theme" style="opacity: 1; display: block;"> 

          <div class="owl-wrapper-outer">
           <div class="owl-wrapper" style="left: 0px; display: block;">
           
           
            <div class="owl-item" style="position:relative;width: 100%" v-for="(TabCarousel,Idx) in TabCarousel" v-if="CurCarousel == Idx">
             <div class="carouselContent1 W"> 
              <div class="item"> 
               <div class="item-img lazyOwl" img-src="http://139.196.232.21/images/vmware-ibm-selected.png" tab-name-track="" :style="{display: 'block',backgroundImage:'url('+ TabCarousel.img +')'}"></div> 
               <div class="l2_banner_content colorWhite"> 
                <h2>{{TabCarousel.title}}</h2> 
                <p>{{TabCarousel.content}}</p> 
                <a class="btn btn-orangered"  href="linguo.jsp">{{TabCarousel.link}}</a> 
               </div> 
              </div>
             </div>
            </div>

           </div>
          </div> 
          
          
          
          <div class="owl-controls clickable">
           <div class="owl-pagination">
            <div :class="{'owl-page':true,'active':CurCarousel == Idx}" v-for="(TabCarousel,Idx) in TabCarousel" @click="ChangeCurCarousel(Idx)">
             <span class="CursorPointer"><img :src="TabCarousel.sloganImg" alt="" /></span>
            </div>
            <!-- <div class="owl-page ">
             <span class=""><img src="http://139.196.232.21/images/logo-zpmc.png" alt="" tab-name-track="baystate_health" /></span>
            </div>
            <div class="owl-page">
             <span class=""><img src="http://139.196.232.21/images/logo-chinapost.png" alt="" tab-name-track="seventy_seven_energy" /></span>
            </div> -->
           </div>
           <div class="owl-buttons">
              <div class="owl-prev" @click="PreCurCarousel"><i class="fa fa-angle-left"></i></div>
              <div class="owl-next" @click="NextCurCarousel"><i class="fa fa-angle-right"></i></div>
            </div>
           <!-- <div class="owl-buttons">
            <div class="owl-prev">
             <i class="fa fa-angle-left"></i>
            </div>
            <div class="owl-next">
             <i class="fa fa-angle-right"></i>
            </div>
           </div> -->
          </div>

         </div> 
        </div> 
       </div> 
      </div> 
     </div> 
    </div> 
   </div> 
  </div>
  </div>
</template>
<script>

  export default{
    data: function () {
      return {
        CurCarousel:1,
        TabCarousel:[
          {'img':'http://139.196.232.21/images/vmware-ibm-increases-agility-with-nsx-automation.jpg','title':'打造企业“智造力”实现企业的卓越价值和基业长青','content':'设计创新力、整合销售力、敏捷制造力、协同运营力4个方面打造企业“智造力”。','link':'','sloganImg':'http://139.196.232.21/images/logo-linguo.png'},
          {'img':'http://139.196.232.21/images/vmware-scaling-to-serve-one-million-patients-a-year.jpg','title':'从传统到智能让制造更简单','content':'Ztnet开发SFIS生产现场管控系统对整个生产过程进行管控，包括物料、生产、品质、重工、维修、包装、入库等，能最大化的提升企业的生产效率。','link':'','sloganImg':'http://139.196.232.21/images/logo-zpmc.png'},
          {'img':'http://139.196.232.21/images/vmware-seventy-seven-energy.jpg','title':'Ztnet 助力上海邮政快速步入”互联网+“ 时代','content':'商业快件平台、跨境电子物流平台让业务更加高效、畅通。','link':'','sloganImg':'http://139.196.232.21/images/logo-chinapost.png'}
        ]

      }
    },
    mounted: function () {
      
    },
    created() {
      
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
      ChangeCurCarousel(Idx){
        this.CurCarousel = Idx
      },
      PreCurCarousel(){
        if(this.CurCarousel>0){
          this.CurCarousel-=1
        }else{
          this.CurCarousel = 2
        }
      },
      NextCurCarousel(){
        if(this.CurCarousel<2){
          this.CurCarousel+=1
        }else{
          this.CurCarousel = 0
        }
      },
     

    }
  }
</script>
<style lang="scss">
.TabCarousel{

}
</style>
