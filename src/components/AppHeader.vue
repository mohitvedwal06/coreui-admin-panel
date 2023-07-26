<template>
    <div class="MainContainer">
     <div class="first ">
        <div class="inner">
            <p><fa icon="bars" class="text-dark"/></p>
            <p>Dashboard</p>
            <p>Users</p>
            <p>Settings</p>
        </div>
     </div>
     <div class="second">
     </div>
     <div class="third">
       <div class="innerThird">
        <p><fa icon="bell" class="text-dark"/></p>
        <p><fa icon="list" class="text-dark"/></p>
        <p><fa icon="envelope-open" class="text-dark"/></p>
        <p><fa icon="user-circle" class="text-dark" id="profile"/></p>
       </div>
     </div>
    </div>
</template>

<script>
    export default {
        setup(){

        }
    }
</script>

<style>
.MainContainer{
    display: flex;
    padding-top: 1%;
    padding-bottom: 1%;
    border-bottom: 1px solid;
}
.first{
    /* border: 1px solid black; */
    display: flex;
    justify-content: center;
    align-items: center;
    padding-left: 2%;
    width: 21%;
}
.inner{
    display: flex;
    width: 100%;
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
    /* border: 1px solid black; */
    display: flex;
    justify-content: center;
    align-items: center;
    padding-left: 2%;
    width: 21%;
}
.innerThird{
    display: flex;
    width: 100%;
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

</style>