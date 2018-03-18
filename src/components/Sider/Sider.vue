<template>
  <div>
    <div class="desktop">
      <Menu :theme="theme3" :active-name="CurSiderMenu" @on-select="ChangeSiderMenu">
          <MenuGroup title="">
              <MenuItem name="HER云平台" class="marginB_20">
                  <Icon size="22" type="ios-cloud"></Icon>
                  <h5>HER云平台</h5>
              </MenuItem>
              <MenuItem name="公司" class="marginB_20">
                  <i class="F_24 fa fa-building" aria-hidden="true"></i>
                  <h5>公司</h5>
              </MenuItem>
          </MenuGroup>
      </Menu>
    </div>
    <div class="tablet">
      <Menu :theme="theme3" :active-name="CurSiderMenu" @on-select="ChangeSiderMenu2">
          <MenuGroup title="">
              <MenuItem name="HER云平台" class="marginB_20">
                  <Icon size="22" type="ios-cloud"></Icon>
                  <h5>HER云平台</h5>
              </MenuItem>
              <MenuItem name="公司" class="marginB_20">
                  <i class="F_24 fa fa-building" aria-hidden="true"></i>
                  <h5>公司</h5>
              </MenuItem>
          </MenuGroup>
      </Menu>
    </div>
  </div>
</template>
<script>

  export default{
    data: function () {
      return {
        theme3: 'light'
      }
    },
    mounted: function () {
      
    },
    created() {
      
    },
    computed: {
      CurSiderMenu(){
        return this.$store.state.CurSiderMenu
      }
      
    },
    watch: {
      
    },
    components: {
      

    },
    methods: {
      ChangeSiderMenu(Menu){
        this.$store.state.CurSiderMenu = Menu
        this.$router.push({name:Menu})
        //this.ToggleSider()
      },
      ChangeSiderMenu2(Menu){
        this.$store.state.CurSiderMenu = Menu
        this.$router.push({name:Menu})
        this.ToggleSider()
      },
      ToggleSider (flag) {
          this.$store.state.open = !this.$store.state.open
      },
     

    }
  }
</script>
<style lang="scss">
.F_24{
  font-size: 22px;
}
.desktop{
  display: none;
}
.tablet{
  display: inline-block;
}
@media (min-width: 769px) {
  .desktop{
    display: inline-block;
  }
  .tablet{
    display: none !important;
  }

}
.ivu-menu-item-group-title{
  background-repeat: no-repeat;
  background-position-x: center;
  background-image: url('http://139.196.232.21/images/logo.png')
}
.ivu-menu-light{
  width: 150px !important;
}
</style>
