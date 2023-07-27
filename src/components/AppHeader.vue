<template>
    <div class="MainContainer">
     <div :class="!isTrue ? 'first' : 'headerContent'">
        <div class="inner">
            <button id="hamburgerMenu-btn" class="bg-transparent" @click="moveSideBar"><fa icon="bars" class="text-dark"/></button>
            <p>Dashboard</p>
            <p>Users</p>
            <p>Settings</p>
        </div>
    </div>
    <div v-if="isShown" :class= "!isTrue ? 'profileDropdown': 'profileDropdowns'">
      <ProfileDropdown />
    </div>
     <div class="second">
     </div>
     <div :class="!isTrue ? 'third' : 'headerLinks'">
       <div class="innerThird">
        <p><fa icon="bell" class="text-dark"/></p>
        <p><fa icon="list" class="text-dark"/></p>
        <p><fa icon="envelope-open" class="text-dark"/></p>
        <p><fa icon="user-circle" class="text-dark" id="profile"  @click="clicked"/></p>
        {{ console.log("isTrue", this.isTrue) }}
       </div>
     </div>
    </div>
</template>

<script>
import ProfileDropdown from './ProfileDropdown.vue';

    export default {
        data() {
            return {
                isTrue : false,
                isShown:false
            }
        },
        components:{
            ProfileDropdown
        },
        methods: {
            moveSideBar() {
                if(this.isTrue===true){
                    this.isTrue = false;
                    this.isShown=false;
                    this.$emit('hideShowSidebar',{
                        isTrue: this.isTrue,
                        
                    });
                }
                else{   
                    this.isTrue = true;
                    this.isShown=false;
                    this.$emit('hideShowSidebar',{
                        isTrue: this.isTrue,
                    });               
                }
            },
            clicked(){
                  if(this.isShown===false)
                  {
                    this.isShown=true
                  }
                  else{
                    this.isShown=false
                  }
            }
        }
    }
</script>

<style>
.MainContainer{
    display: flex;
    padding-top: 1%;
    padding-bottom: 1%;
    border-bottom: 1px solid;
    width: 100%;
    height:10vh;
    align-items:center;
    justify-content: space-between;
}
.first{
    padding-left: 20px; 
}
.inner{
    display: flex;
    width: 251px;
    justify-content: center;
    align-items: center;
}
.inner p{
    margin:0px 8px 0px 8px;
}
.third{
    padding-right: 25px;
}
.innerThird{
    display: flex;
    width: 220px;
    justify-content: center;
    align-items: center;
    justify-content: space-between;
}
.innerThird p{
    margin: 0;
    font-size: 24px;
}
#profile{
    font-size: 40px;
}
.headerContent{
    padding-left:20px;
}
.headerLinks{
    padding-right:25px;
}
#hamburgerMenu-btn{
    border: none;
}
.profileDropdown{
    width: 18%;
    border-radius: 4px;
    font-size: .79rem;
    line-height: 1rem;
    float: right;
    position: relative;
    z-index: 999;
    box-shadow: 1px 1px 12px -9px;
    border: 1px groove grey;
    left: 26rem !important;
    top: 14.79rem;
}
.profileDropdowns{
    width: 16%;
    border-radius: 4px;
    font-size: .79rem;
    line-height: 1rem;
    float: right;
    position: relative;
    z-index: 999;
    box-shadow: 1px 1px 12px -9px;
    border: 1px groove grey;
    left: 36rem !important;
    top: 15rem;
}

</style>