<template>
    <div class="tabs">
        <div class="nav-tabs">
            <p class="nav-item" @click="setActive('tab-1')" :class="{ 'active' : isActive('tab-1') }">Tab 1</p>
            <p class="nav-item" @click="setActive('tab-2')" :class="{ 'active' : isActive('tab-2') }">Tab 2</p>
        </div>
        <div class="tab-content">
            <div class="tab-pane" v-show="isActive('tab-1')">
                <div class="for-example">
                    <p>- qwqwq</p>
                    <p>- qweqwweqwe</p>
                    <p>- qweqwweqwe</p>
                    <p>- qweqweqwe</p>
                    <p>- qweqweqwe</p>
                </div>
            </div>
            <div class="tab-pane" v-show="isActive('tab-2')">
                <div class="for-example">
                    <p>- eweweew</p>
                    <p>- wewewewew</p>
                    <p>- weweweqw</p>
                    <p>- wewewewewewew</p>
                    <p>- wewewe</p>
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
.tab-pane {
    max-width: 300px;
    width: 100%;
}
</style>