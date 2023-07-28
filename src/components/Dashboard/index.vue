<template lang="">
    <div id="dashboard" class="mt-4 p-3">
        <div id="dashboard-graphs" class="d-flex justify-content-evenly">
            <div class="graphs-div text-white" v-for="(item,index) in companyData" :key="index" :style="{backgroundColor: item.color}">
                <h5>
                    <b>{{item.rate}}</b> <span class="fs-6">({{item.growth}} <fa :icon="item.growthIcon"/>)</span>
                </h5>
                <p>{{item.title}}</p>
                <img class="graph-img ms-3" src = "../../assets/graph.png"/>
            </div>
        </div>
        <div id="traffic" class="mx-auto mt-4 p-3 bg-white">
            <div class="traffic-header d-flex justify-content-between">
                <div id="traffic-heading">
                    <h4><b>Traffic</b></h4>
                    <span class="ms-1">July 2023</span>
                </div>
                <div>
                    <div class="btn-group traffic-btn" role="group" aria-label="Basic example">
                        <button type="button" class="btn btn-secondary pt-2 pb-2">Day</button>
                        <button type="button" class="btn btn-secondary pt-2 pb-2">Month</button>
                        <button type="button" class="btn btn-secondary pt-2 pb-2 ">Year</button>
                    </div>
                </div>
            </div>
            <img class="traffic-graph-img" src="../../assets/traffic-graph.png"/>
        </div>
        <div class="traffic-footer d-flex justify-content-between mx-auto pt-3 px-4 pb-3 text-center">
            <div v-for="(item,index) in activites" :key="index">
                <p>{{item.title}}</p>
                <p><b>{{item.rate}} {{item.activity}} ({{item.growth}})</b></p>
                <div id="progress-bar">
                    <div :class=item.progressBarWidth :style={backgroundColor:item.progressBarColor}></div>
                </div>
            </div>
        </div>
        <div>
            
        </div>
        <!-- <div class="traffic-Sales mx-auto pt-2 pb-3">
            <div class="traffic-Sales-heading">
                <p>Traffic & Sales</p>
            </div>
            <div>

            </div>
        </div> -->
    </div>
</template>
<script>
export default {
    data(){
        return {
            companyData : [
                {
                    rate: "26K",
                    growth : "-12.4%",
                    title: "Users",
                    color: "#2f5597",
                    growthIcon: "arrow-down",
                },
                {
                    rate: "$6.200",
                    growth : "40.9%",
                    title: "Income",
                    color: "#ffd966",
                    growthIcon: "arrow-up"
                },
                {
                    rate: "2.49%",
                    growth : "84.7%",
                    title: "Conversion Rate",
                    color: "#00b050",
                    growthIcon: "arrow-up"
                },
                {
                    rate: "44K",
                    growth : "-23.6%",
                    title: "Sessions",
                    color: "#7e0021",
                    growthIcon: "arrow-down"
                },
            ],
            activites: [
                {
                    title: "Visits",
                    rate: "29.703",
                    growth: "40%",
                    activity: "Users",
                    progressBarWidth: "w-40",
                    progressBarColor: "#2f5597"
                },
                {
                    title: "Unique",
                    rate: "24.093",
                    growth: "20%",
                    activity: "Users",
                    progressBarWidth: "w-25",
                    progressBarColor: "#ffd966"
                },
                {
                    title: "Pageviews",
                    rate: "78.706",
                    growth: "60%",
                    activity: "Views",
                    progressBarWidth: "w-75",
                    progressBarColor: "#00b050"
                },
                {
                    title: "New Users",
                    rate: "22.123",
                    growth: "80%",
                    activity: "Users",
                    progressBarWidth: "w-75",
                    progressBarColor: "#7e0021"
                },
                {
                    title: "Bounce Rate",
                    growth: "40.15%",
                    activity: "Average Rate",
                    progressBarWidth: "w-40",
                    progressBarColor: "#f68024"
                },
            ],
        }   
    },
}
</script>
<style>
    #dashboard{
        width:100%;
        height:91vh;
        overflow-y: scroll;
        background-color: #ebedef;
    }
    #dashboard::-webkit-scrollbar{
        display:none;
    }
    #dashboard-graphs div{
        padding:20px;
        border-radius:10px;
    }
    .graphs-div{
        width:230px;
    }
    .graph-img{
        width:150px;
        height:90px;
    }
    #traffic{
        width: 95%;
        border-top-left-radius: 10px;
        border-top-right-radius: 10px;
        box-shadow: 0px 0px 1px #444444;
    }
    .traffic-btn button{
        background-color: white;
        color:black;
    }
    .traffic-btn button:hover{
        background-color:grey; 
    }
    .traffic-graph-img{
        width:100%;
    }
    #traffic-heading{
        line-height: 10px;
    }
    #traffic-heading span{
        font-size:14px;
    }
    .traffic-footer{
        width:95%;
        border-bottom-left-radius: 10px;
        border-bottom-right-radius: 10px;
        box-shadow: 0px 0px 2px #444444;
        line-height: 13px;
        background-color:#f7f7f8;
    }
    #progress-bar{
        border-radius:10px;
        background-color: #c6c6c6;
    }
    #progress-bar div{
        padding:2px;
        border-radius:10px;
        width:40%;
    }
    .traffic-Sales{
        border: 1px solid;
        width: 95%;
    }
    .traffic-Sales-heading{
        border-bottom: 1px solid;
    }
</style>