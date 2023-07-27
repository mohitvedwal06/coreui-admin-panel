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
     <div class="second">
     </div>
     <div :class="!isTrue ? 'third' : 'headerLinks'">
       <div class="innerThird">
        <p><fa icon="bell" class="text-dark"/></p>
        <p><fa icon="list" class="text-dark"/></p>
        <p><fa icon="envelope-open" class="text-dark"/></p>
        <p><fa icon="user-circle" class="text-dark" id="profile"/></p>
        {{ console.log("isTrue", this.isTrue) }}
       </div>
     </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                isTrue : false,
            }
        },
        methods: {
            moveSideBar() {
                if(this.isTrue===true){
                    this.isTrue = false;
                    this.$emit('hideShowSidebar',{
                        isTrue: this.isTrue,
                    });
                }
                else{   
                    this.isTrue = true;
                    this.$emit('hideShowSidebar',{
                        isTrue: this.isTrue,
                    });               
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
    /* position:relative; */
    width: 100%;
    height:13vh;
    align-items:center;
}
.first{
    /* border: 1px solid black; */
    padding-left: 20px; 
    /* width: 21%; */
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
.second{
    /* border: 1px solid black; */
    width: 58%;
}
.third{
    /* width: 21%; */
    padding-right: 25px;
}
.innerThird{
    display: flex;
    width: 220px;
    justify-content: center;
    align-items: center;
}
.innerThird p{
    margin: 0px 16px 0px 14px;
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

</style>