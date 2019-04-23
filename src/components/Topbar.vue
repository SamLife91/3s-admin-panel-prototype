<template>
  <div class="topbar">
    <div class="container">
      <div class="col">
        <div class="el title">
          LOGO
        </div>
        <div class="el breadcrumb">
          LOREM > LOREM
        </div>
      </div>
      <div class="col">
        <div class="el user">
        <img src="@/assets/icn/user-solid.svg" alt="">
        Lorem, ipsum dolor.
      </div>
        <div class="el lang">
          <img src="@/assets/icn/globe-europe-solid.svg" alt="">
          Lorem, ipsum.
      </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  
}
</script>

<style lang="scss" scoped>
.topbar {
  display: flex;
  height: 55px;
  background-color: #fff;
  box-shadow: 0px 0px 1px 0px black;
  justify-content: center;
  .container {
    width: 90%;
    display: flex;
  }
}
.topbar .container {
  
  
  .col {
    display: flex;
    flex: 1;
    justify-content: center;
    align-items: center;
    flex-direction: row;
    .el {
      // flex: 1;
    }
  }
  .col:nth-child(1) {
    justify-content: flex-start;
    .title {
      // flex: 1;
    }
    .breadcrumb {
      font-size: 11px;
      text-transform: uppercase;
    }
  }
  .col:nth-child(2) {
    justify-content: flex-end;
    font-size: 14px;
    img {
      display: block;
      height: 20px;
      margin: 0 1vw;
    }
    .user, .lang {
      display: flex;
      align-items: center;
      cursor: pointer;
    }
    .user {
      border-right: 1px solid #000;
      padding-right: 1.8vw;
    }
    .lang {
      border-left: 1px solid #000;
      padding-left: 1.8vw;
    }
  }
  .title, .breadcrumb {
    
  }
  .user, .lang {
    
  }
}
</style>

