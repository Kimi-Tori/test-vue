<template>
    <div class="tabs">
        <div class="nav-tabs">
            <p class="nav-item" @click="setActive('tab-1')" :class="{ 'active' : isActive('tab-1') }">Tab 1</p>
            <p class="nav-item" @click="setActive('tab-2')" :class="{ 'active' : isActive('tab-2') }">Tab 2</p>
        </div>
        <div class="tab-content">
            <div class="tab-pane" v-show="isActive('tab-1')">
                <div class="for-example">
                    <p>A superhero is a character endowed with extraordinary abilities ("superpowers"), which he uses to accomplish feats in the name of the common good. After the debut of a prototypical superhero named Superman in 1938, the idea of a superhero — from brief, episodic adventure stories to long—term and multi-part sagas - became dominant in American comics, from which it subsequently spread to other formats of fiction.</p>
                </div>
            </div>
            <div class="tab-pane" v-show="isActive('tab-2')">
                <div class="for-example">
                    <p>Package name - 5.7 AT Z28 SS</p>
                    <p>Release period - 1995 - 1997</p>
                    <p>Type of drive - Задний</p>
                    <p>Body type - Открытый кузов</p>
                    <p>Transmission type - АКПП 4</p>
                    <p>Engine volume, cc - куб.см	5733</p>
                    <p>Acceleration time 0-100 km/h, s - с	6.3</p>
                    <p>Maximum speed, km/h - км/ч	250</p>
                    <p>Ground clearance (road clearance), mm - мм	124</p>
                    <p>Assembly country - Канада</p>
                    <p>Number of doors - 2</p>
                    <p>Manufacturer's Warranty - 3 года или 36 000 миль пробега</p>
                    <p>Тех. характеристик супергероев увы не было</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'TabsComponent',
  props: {
    msg: String
  },
  data : () => ({
    activeTab: 'tab-1'
  }),
  methods : {
    setActive(tab) {
        this.activeTab = tab
    },
    isActive(tab) {
        return this.activeTab === tab;
    }
  }
}
</script>

<style scoped>
.tabs {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: 30px;
}
.nav-tabs {
    display: flex;
    justify-content: center;
}
.nav-item {
    padding: 10px 20px;
    background-color: #232c4b;
    border-radius: 20px 20px 0 0;
    cursor: pointer;
    margin-right: 10px;
    border: 2px solid #0c1124;
    border-bottom: none;
    transition: 0.3s ease;
}
.nav-item:last-child {
    margin-right: 0;
}
.active {
    background-color: #0c1124;
}
.tab-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: #232c4b;
    padding: 20px;
    border: 2px solid #0c1124;
    border-radius: 20px;
    width: calc(100% - 44px);
    min-height: 200px;
}
.for-example p {
    margin: 2.5px 0;
}
.tab-pane {
    max-width: 500px;
    width: 100%;
}
</style>