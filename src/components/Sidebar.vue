<template>
  <div class="sidebar">
    <div class="head">

    </div>
    <div class="menu">
      <div class="link" v-for="(link, index) in links" :key='index'>
        <div class="row">
          <span class="title">
            {{link.name }}
          </span>
          <span class="icn">
            <img :src="require(`@/assets/icn/${link.icn}.svg`)" alt="">
          </span>
        </div>
        <div class="row dropdown" v-if="Array.isArray(link.submenu)">
          <div class="submenu" v-for="(sub, index) in link.submenu" :key="index">
              <span class="title">
                {{sub.name}}
              </span>
              <span class="icn">
                <img :src="require(`@/assets/icn/${sub.icn}.svg`)" alt="">
              </span>
            </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      links: [
        {name: 'lorem', icn: 'sitemap-solid'},
        {name: 'lorem', icn: 'home-solid'},
        {name: 'lorem', icn: 'envelope-open-regular'},
        {name: 'lorem', icn: 'user-circle-regular'},
        {name: 'lorem', icn: 'sitemap-solid', submenu: [
          { name: 'sub1', icn: 'sitemap-solid'},
          { name: 'sub2', icn: 'sitemap-solid'}
        ]},
        {name: 'lorem', icn: 'home-solid', submenu: [
          {name: 'sub1', icn: 'home-solid'},
          {name: 'sub2', icn: 'home-solid'}
        ]},
        {name: 'lorem', icn: 'envelope-open-regular'},
        {name: 'lorem', icn: 'user-circle-regular'},
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/styles/_vars.scss';
.sidebar {
  height: 100vh;
  background-color: #2a303b;
  color: #626262;
  display: flex;
  flex-direction: column;
  .head {
      background-color: #272b35;
      height: 55px;
    }
    .menu {
      flex: 3;
      .link {
        display: flex;
        font-size: 20px;
        align-items: center;
        cursor: pointer;
        flex-direction: column;
        .row {
          display: flex;
          flex-direction: row;
          margin: .2vw;
          justify-content: space-between;
          width: 100%;
          align-items: center;
          .submenu {
            // display: flex;
            width: 100%;
            justify-content: space-between;
          }
        }
        .dropdown {
          display: flex;
          flex-direction: column;
          .submenu {
            width: 100%;
            display: inherit;
            flex-direction: row;
            background-color: $darker;
            align-items: center;
          }
        }
        .title {
          font-size: 14px;
          text-transform: capitalize;
        }
        .icn {
          width: 40px;
          height: 40px;
          background-color: $darker;
          display: flex;
          align-items: center;
          flex-direction: column;
          justify-content: center;
          img {
            height: 14px;
            width: 14px;
          }
        }
        &:hover {
        > .row:first-child {
          color: #fff;
           img {
            filter: invert(1);
          }
        }
        }
        .submenu:hover {
          color: $white;
        }
      }
    }
  
}
</style>

