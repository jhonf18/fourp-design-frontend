<template>
  <div class="tabs-container">
    <div class="tabs">
      <ul v-if="!tabsBp">
        <li :key="index" v-for="(tab, index) in tabs" :class="{ 'is-active': tab.isActive }" >
          <a :href="tab.href" @click="selectTab(tab)" >{{ tab.name }}</a>
        </li>
      </ul>
    </div>
    <div >
      <div class="tabs-details">
        <slot></slot>
      </div>
    </div>
    <Helper v-if="tabsBp" :home="true">
      <ul style="display:block; overflow-y: scroll; max-height: 230px;" >
        <li v-for="(tab, index) in tabs" :class="{ 'is-active': tab.isActive }"  :key="index">
          <a :href="tab.href" @click="selectTab(tab)" >{{ tab.name }}</a>
        </li>
      </ul>
    </Helper>
  </div>
</template>

<script>

export default {
  name: 'Tabs',
  props: {
    container: Boolean
  },
  data() {
    return {
      tabs: [],
      cont: 0,
      tabsBp: false
    };
  },
  created(){
    this.tabs = this.$children;
    if (process.browser) {
      const tabsBp = matchMedia('(max-width: 925px)');
      const changeSize = mql => {
        mql.matches
          ? this.tabsBp = true
          : this.tabsBp = false
      }
      tabsBp.addListener(changeSize);
      changeSize(tabsBp);
    }


  },
  mounted(){
    this.searchTab(this.$route.hash);
  },
  methods: {
    selectTab(selectedTab) {
      this.tabs.forEach(tab => {
        tab.isActive = (tab.name == selectedTab.name);
      });
    },
    searchTab(hash) {
      if(hash == '' || !hash){
        let int = setInterval(()=> {
          if(this.tabs){
            this.selectTab(this.tabs[0]);
            clearInterval(int)
          }
        }, 500)
      } else {
        let int = setInterval(()=> {
          for( let i in this.tabs){
            if(this.tabs[i].href == hash){
              this.selectTab(this.tabs[i]);
              clearInterval(int);
              break;
            }
          }
        }, 500)
      }
    }
  }
}
</script>

<style lang="scss" scoped src="../assets/css/Tabs.scss" ></style>
