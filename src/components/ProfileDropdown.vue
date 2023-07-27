<template>
    <div id="mainContainer">
    <p id="heading">Account</p>
    <p class="innerComponent ps-2"><fa icon="bell" class="text-dark me-1" />Updates</p>
    <p class="innerComponent ps-2"><fa icon="message" class="text-dark me-1"/>Message</p>
    <p class="innerComponent ps-2"><fa icon="tasks" class="text-dark me-1"/>Tasks</p>
    <p class="innerComponent ps-2"><fa icon="comment" class="text-dark me-1"/>Comments</p>

    <p id="headingg">Setting</p>
    <p class="innerComponent ps-2"><fa icon="user" class="text-dark me-1"/>Profile</p>
    <p class="innerComponent ps-2"><fa icon="gear" class="text-dark me-1"/>Setting</p>
    <p class="innerComponent ps-2"><fa icon="dollar-sign" class="text-dark me-1"/>Payments</p>
    <p class="innerComponent ps-2 "><fa icon="file" class="text-dark me-1"/>File</p>
    <p class="lastItem"></p>
    <p class="innerComponent ps-2"><fa icon="shield-halved" class="text-dark me-1"/>Lock Account</p>
    <p class="innerComponent ps-2"><fa icon="lock" class="text-dark me-1"/>Logout</p>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped >
#mainContainer{
    /* border: 1px solid black; */
    /* width: 35%;
    border-radius: 4px;
    font-size: .79rem;
    line-height: 1rem;
    float: right;
    margin-top: -14px;
    position: relative;
    margin-right: 51px;
    z-index: 999;
    box-shadow: 1px 1px 12px -9px;
    border: 1px groove grey;
    left: 34rem !important;
    top: 15.5rem;*/
}
.block_one{
    border: 1px solid black;
}
#heading
{
    width: 100%;
    padding: 4%;
    font-size: 14px;
    font-weight: 600;
    padding-left: 10%;
    background-color: #ebedef;
    color: #8a93a2;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
}
#headingg
{
    width: 100%;
    padding: 4%;
    font-size: 14px;
    font-weight: 600;
    padding-left: 10%;
    background-color: #ebedef;
    color: #8a93a2;
}
.innerComponent{

}
.lastItem
{
    border-bottom: 1px solid;
}
</style>

 <!-- <div class="block_one">
        <div><p>Account</p></div>
        <p><fa icon="bell" class="text-dark"/>Updates</p>
        <p><fa icon="message" class="text-dark"/>Message</p>
        <p><fa icon="tasks" class="text-dark"/>Tasks</p>
        <p><fa icon="comment" class="text-dark"/>Comments</p>
     </div>

     <div>
        <div><h6>Setting</h6></div>
        <p><fa icon="user" class="text-dark"/>Profile</p>
        <p><fa icon="gear" class="text-dark"/>Setting</p>
        <p><fa icon="dollar-sign" class="text-dark"/>Payments</p>
        <p><fa icon="file" class="text-dark"/>File</p>
     </div>

     <p><fa icon="shield-halved" class="text-dark"/>Lock Account</p>
     <p><fa icon="lock" class="text-dark"/>Logout</p> -->