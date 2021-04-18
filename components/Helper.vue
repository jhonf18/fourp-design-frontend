<template>
    <div :class="{ 'theme-helper': true, 'theme-helper-opened': opened, 'sticky': sticky,
    }">
        <section class="widget theme-helper-content" :class="{'bg-dark': home}">
            <header class="theme-helper-header flex p-0">
                <div class="theme-helper-toggler" @click="toggle">
                    <div class="theme-helper-spinner bg-categories text-white"
                      :class="{ 'bg-categories-home': home  }">
                        <svg class="icon-th text-white" width="25px" style="margin: 5px -2px" height="25px" ><use xlink:href="#icon-th"></use></svg>
                    </div>
                </div>
                <h5>Categorias</h5>
            </header>
            <div class="widget-body mt-.5 ">
              <slot></slot>
            </div>

        </section>
    </div>
</template>

<script>
export default {
  props: {
    home: {
      type: Boolean,
      default: false
    },
  },
  data() {
    return {
      opened: false,
      sticky: false
    }
  },
  mounted() {
    let sticky = false;

    if (process.browser) {
      const isBottom = ()=> {
      // console.log('scroll', $(window).scrollTop())
      // console.log('heigy', $('.content-top').height())
      var elmnt = document.getElementsByClassName("content-top")[0];
        return window.scrollTop + 55 > elmnt.offsetHeight;
      }

      window.addEventListener('scroll', ()=> {
        const inBottom = isBottom();

        if(inBottom && !sticky) {
          this.sticky = true;
          sticky = true;
        }
        if(!inBottom && sticky)  {
          this.sticky = false;
          sticky = false;
        }
      })
    }


  },
  methods: {
    toggle() {
      this.opened = !this.opened;
    }
  }
};
</script>

<style src="../assets/css/Helper.scss" lang="scss" scoped />
