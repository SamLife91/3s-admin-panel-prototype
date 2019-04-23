<template>
  <div>
    <div class="top">
      <div class="shell">
        <div class="item page_title">
          page title
        </div>
        <div class="item page_actions">
          <button>
            action
          </button>
        </div>
      </div>
    </div>
    <hr>
    <div class="content">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Blanditiis, voluptate!
    </div>
  </div>
</template>

<script>
export default {
  
}
</script>
<style lang="scss" scoped>
.top {
   background-color: #f0f0f0;
}
.shell {
  align-items: center;
  padding: 1.5vh 4vw;
  display: flex;
  > .item {
    flex: 1;
    text-align: left;
  }
  .item:nth-child(2) {
    text-align: right;
  }
}
.page_title {
  font-size: 31px;
  font-weight: 300;
  color: #2c2c2c;
  text-transform: uppercase;
}
</style>

