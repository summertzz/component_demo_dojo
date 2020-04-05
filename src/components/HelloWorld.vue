<template>
<div class="jd-page-container">
  <!-- 菜单栏导航 -->
  <div class="jd-content-box">
    <div class="jd-col-box">
      <ul>
        <li v-for="(navItem, navIndex) in menuConfig" :key="navIndex" 
        @mouseenter="handleShowInfosBox(navItem)"
        @mouseleave="handleHideInfosBox"
        >
          <template v-for="(navSubItem, navSubIndex) in navItem.side">
            <template v-if="navSubIndex !== 0"> /  </template>
           <a :href="navSubItem.link" :key="navSubIndex"> {{ navSubItem.label}}</a>
          </template>
        </li>
      </ul>
    </div>
    <div class="jd-col-box"></div>
    <div class="jd-col-box"></div>
    <div class="jd-col-box"></div>
  </div>
  <!-- 菜单栏详情-->
  <div class="jd-nav-detail-box" v-if="infosBoxVisible" @mouseenter="handleMounseEnterInfosBox" @mouseleave="handleMouseLeaveInfosBox">
    <div class="top-nav-infos">
      <template v-for="(topNvaItem, topNavIndex) in activeInfos.topNavInfos">
        <a href="" :key="topNavIndex"> {{ topNvaItem.label}} > </a>
      </template>
    </div>
    <div class="main-nav-infos" v-for="(mainNavItem, mainNavIndex) in activeInfos.mainNavInfos" :key="mainNavIndex +'main'">
      <strong>{{mainNavItem.label}} > </strong>
      <template v-for="(mainNavSubItem, mainNavSubIndex) in mainNavItem.children">
        <span :key="mainNavSubIndex + 'sub'"> {{ mainNavSubItem.label }}</span>
      </template>
    </div>
  </div>
</div>

</template>
<script>
export default {
  data() {
    return {
      isSideMounseEnter: false,
      isDetailInfosBoxMouseEnter: false,
      activeInfos: '',
      menuConfig: [
        {
          side:[
            {
              label: '女鞋',
              link: '女鞋',
            },
          ],
          infos: {
            topNavInfos: [
              {
                label: '企业采购',
                link: '企业采购',
              },
              {
                label: '商用电器',
                link: '商用电器',
              },
              {
                label: '美迪惠尔',
                link: '燃气热水器',
              },
              {
                label: '咖啡机',
                link: '咖啡机',
              },
              {
                label: '洗面奶',
                link: '洗面奶',
              },
            ],
            mainNavInfos: [
              {
                label: '香水彩妆',
                link: '香水彩妆',
                children: [
                  {
                    label: '隔离',
                    link: '隔离',
                  },
                  {
                    label: '遮瑕',
                    link: '遮瑕',
                  },
                  {
                    label: '气垫BB',
                    link: '气垫BB',
                  },
                  {
                    label: '神仙水儿',
                    link: '神仙水儿',
                  },
                  {
                    label: '隔离',
                    link: '隔离',
                  },
                ]
              }
            ],
            adsNavInfos: [],
          },
        },
         {
          side:[
            {
              label: '箱包',
              link: '箱包',
            },
            {
              label: '钟表',
              link: '钟表',
            },
            {
              label: '个护清洁',
              link: '个护清洁',
            },
          ],
             infos: {
            topNavInfos: [
              {
                label: '面膜',
                link: '面膜',
              },
              {
                label: '雅诗兰黛',
                link: '雅诗兰黛',
              },
              {
                label: '美迪惠尔',
                link: '美迪惠尔',
              },
              {
                label: '咖啡机',
                link: '咖啡机',
              },
              {
                label: '洗面奶',
                link: '洗面奶',
              },
            ],
            mainNavInfos: [
              {
                label: '香水想想',
                link: '香水',
                children: [
                  {
                    label: '隔离霜',
                    link: '隔离霜',
                  },
                  {
                    label: '遮瑕',
                    link: '遮瑕',
                  },
                  {
                    label: '气垫BB1',
                    link: '气垫BB1',
                  },
                  {
                    label: '神仙水儿1',
                    link: '神仙水儿1',
                  },
                  {
                    label: '隔离',
                    link: '隔离',
                  },
                ]
              },
               {
                label: '香水11',
                link: '香水',
                children: [
                  {
                    label: '隔离霜',
                    link: '隔离霜',
                  },
                  {
                    label: '遮瑕',
                    link: '遮瑕',
                  },
                  {
                    label: '气垫BB1',
                    link: '气垫BB1',
                  },
                  {
                    label: '神仙水儿1',
                    link: '神仙水儿1',
                  },
                  {
                    label: '气垫BB1',
                    link: '气垫BB1',
                  },
                  {
                    label: '神仙水儿1',
                    link: '神仙水儿1',
                  },
                  {
                    label: '气垫BB1',
                    link: '气垫BB1',
                  },
                  {
                    label: '神仙水儿1',
                    link: '神仙水儿1',
                  },
                  {
                    label: '气垫BB1',
                    link: '气垫BB1',
                  },
                  {
                    label: '神仙水儿1',
                    link: '神仙水儿1',
                  },
                  {
                    label: '气垫BB1',
                    link: '气垫BB1',
                  },
                  {
                    label: '神仙水儿1',
                    link: '神仙水儿1',
                  },
                  {
                    label: '气垫BB1',
                    link: '气垫BB1',
                  },
                  {
                    label: '神仙水儿1',
                    link: '神仙水儿1',
                  },
                  {
                    label: '气垫BB1',
                    link: '气垫BB1',
                  },
                  {
                    label: '神仙水儿1',
                    link: '神仙水儿1',
                  },
                  {
                    label: '隔离',
                    link: '隔离',
                  },
                ]
              },
            ],
            adsNavInfos: [],
          },
        }
      ]
    }
  },
  computed: {
    infosBoxVisible() {
      if(this.isSideMounseEnter || this.isDetailInfosBoxMouseEnter) return true;
      return false;
    }
  },
  methods: {
    handleShowInfosBox(config) {
      this.isSideMounseEnter = true;
      this.activeInfos = config.infos;
    },
    handleHideInfosBox() {
      this.isSideMounseEnter = false;
    },
    handleMounseEnterInfosBox() {
      this.isDetailInfosBoxMouseEnter = true;
    },
    handleMouseLeaveInfosBox() {
      this.isDetailInfosBoxMouseEnter = false;
    }
  }
}
</script>
<style lang="scss" scoped>
.jd-page-container {
  .jd-content-box {
    display: flex;
    position: absolute;
    left: 0;
    top: 0;

    width: 1190px;
    height: 480px;

    // transform: translate(-50%);
    background-color: #f4f4f4;
    border: 1px solid #eee;
    .jd-col-box {
      flex: 1;
      margin-left: 10px;

      background-color: #fff;
    }
    .jd-col-box:nth-child(2) {
      flex: 3;
      position: relative;
    }
    .jd-col-box:nth-child(1) {
      margin-left: 0;
    }

    ul {
      padding: 0;
      list-style: none;
      li {
        display: flex;
        justify-content: flex-start;
        align-items: center;
        padding-left: 18px;
        width: 100%;
        height: 25px;
        line-height: 25px;
        
        font-size: 14px;
        transition: background-color .3s;
        &:hover {
          cursor: pointer;
          background-color: #d9d9d9;
        }
        a {
          margin-right: 2px;
          text-decoration: none;
          color: #666;
          transition: color .3s;
          &:hover {
            color: #c8261c;
          }
        }
      }
    }
  }
  /* 菜单栏详情 */
  .jd-nav-detail-box {
    position: absolute;
    left: 195px;
    top: 0;
    width: 994px;
    height: 480px;
    background-color: #fff;
    box-shadow: 2px 0 5px rgba(0,0,0,.3);

    .top-nav-infos {
      padding: 20px 0px 10px 20px;
      display: flex;
      justify-content: flex-start;
      transition: background .3s;

      a {
        text-decoration: none;
        background: #333;
        color: #fff;
        height: 24px;
        line-height: 24px;

        font-size: 12px;
        padding: 0 10px;
        margin-right: 10px;

        &:hover {
          background: #c8261c;
        }
      }
    }

    .main-nav-infos {
      padding-left:20px;
      display: flex;
      justify-content: flex-start;
      align-items: center;

      &:hover {
       cursor: pointer;
    }
      strong {
        padding-right: 10px;
        font-weight: 700;
        font-size: 12px;
        color: #333;
        transition: color .3s;
        width: 60px;
        text-align: right;
        &:hover {
          color: #c8261c;
        }
      }
      span {
        margin: 0px 3px;
        padding: 7px 0px;

        color: #333;
        font-size: 12px;
        transition: color .3s;
          &:hover {
          color: #c8261c;
        }
      }
    }
  }
}
</style>