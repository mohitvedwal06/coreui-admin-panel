<template lang="">
    <div class="d-flex">
        <div id="sideBar-div">
            <div class="pt-3 ps-3 pb-3 bg-dark" id="sideBar-main-div">
                <div class="d-flex justify-content-center pb-4" id="sideBar-logo">
                    <h2>AM</h2>
                    <h2 class="ms-2">Tutorials</h2>
                </div>
                <div class="sidebar-content-div">
                    <div class="d-flex align-items-center sidebar-content" id="sideBar-contents">
                        <fa icon="dashboard" class="ms-3 ps-4"/>
                        <p class="mt-3 ms-4 ps-2">Dashboard</p>
                    </div>
                    <div class="p-1" id="sideBar-theme">
                        <p class="ms-4 mt-4" id="sideBar-theme-heading">THEME</p>
                        <div class="d-flex align-items-center ms-4 ps-3 pt-3 sidebar-content">
                            <fa icon="droplet" class="mb-3 me-4"/>
                            <p class="ms-3 ps-1">Colors</p>
                        </div>
                        <div class="d-flex align-items-center ms-4 ps-3 mt-3 pt-3 sidebar-content">
                            <fa icon="pen" class="mb-3 me-4"/>
                            <p class="ms-3 ps-1">Typography</p>
                        </div>
                    </div>
                    <div class="p-1" id="sideBar-theme">
                        <p class="ms-4 mt-4" id="sideBar-theme-heading">COMPONENTS</p>
                        <div class="d-flex align-items-center ms-4 ps-3 pt-3 sidebar-content">
                            <fa icon="puzzle-piece" class="mb-3 me-4"/>
                            <p class="ms-3 ps-1">Base</p>
                        </div>
                        <div class="d-flex align-items-center ms-4 ps-3 mt-3 pt-3 sidebar-content">
                            <fa icon="location-arrow" class="mb-3 me-4"/>
                            <p class="ms-3 ps-2">Buttons</p>
                        </div>
                        <div class="d-flex align-items-center ms-4 ps-3 mt-3 pt-3 sidebar-content">
                            <fa icon="file-lines" class="mb-3 me-4"/>
                            <p class="ms-4 ps-1">Forms</p>
                        </div>
                        <div class="d-flex align-items-center ms-4 ps-3 mt-3 pt-3 sidebar-content">
                            <fa icon="chart-pie" class="mb-3 me-3"/>
                            <p class="ms-4 ps-1">Charts</p>
                        </div>
                        <div class="d-flex align-items-center ms-4 ps-3 mt-3 pt-3 sidebar-content">
                            <fa icon="star" class="mb-3 me-4"/>
                            <p class="ms-3 ps-1">Icons</p>
                        </div>
                        <div class="d-flex align-items-center ms-4 ps-3 mt-3 pt-3 sidebar-content">
                            <fa icon="bell" class="mb-3 me-4 ps-1"/>
                            <p class="ms-3 ps-1">Notifications</p>
                        </div>
                        <div class="d-flex align-items-center ms-4 ps-3 mt-3 pt-3 sidebar-content">
                            <fa icon="calculator" class="mb-3 me-4 ms-1"/>
                            <p class="ms-3 ps-2">Widgets</p>
                        </div>
                    </div>
                    <div class="p-1" id="sideBar-theme">
                        <p class="ms-4 mt-4" id="sideBar-theme-heading">EXTRAS</p>
                        <div class="d-flex align-items-center ms-4 ps-3 pt-3 sidebar-content">
                            <fa icon="star" class="mb-3 me-4"/>
                            <p class="ms-3 ps-2">Pages</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div id="secondDiv"></div>
    </div>
</template>

<script>
export default {

}
</script>
<style scoped>
    #sideBar-div{
        width:21.5%;
        position:fixed;
    }
    #secondDiv{
        width:78.5%;
    }
    #sideBar-main-div{
        color:white;
    }
    .sidebar-content-div{
        overflow-y: scroll;
        height:88vh;

    }
    #sideBar-logo h2{
        font-style: italic;
        font-weight: 800;
    }
    /* #sideBar-contents, #sideBar-theme{
        border:1px solid;
    } */
    #sideBar-theme-heading{
        font-weight:700;
    }
    .sidebar-content:hover{
        background-color: rgba(98, 98, 98, 0.929);
    }
</style>