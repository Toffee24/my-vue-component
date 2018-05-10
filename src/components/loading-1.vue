<template>
  <div class="loading">
    <div class="ivu-spin-main"><span class="ivu-spin-dot"></span> <div class="ivu-spin-text">加载中</div></div>
  </div>
</template>
<script type="text/ecmascript-6">
  export default {
    props: {
      title: {
        type: String,
        default: '正在载入...'
      }
    }
  }
</script>
<style scoped lang="scss">
  @keyframes ani-spin-bounce {
    0% {
      -webkit-transform: scale(0);
      transform: scale(0)
    }

    to {
      -webkit-transform: scale(1);
      transform: scale(1);
      opacity: 0
    }
  }
  .loading{
    position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    text-align: center;
    z-index: 1000;
    background-color: hsla(0,0%,100%,.9);
    .ivu-spin-main{
      position: absolute;
      top: 42%;
      left: 50%;
      -webkit-transform: translate(-50%,-50%);
      transform: translate(-50%,-50%);
      .ivu-spin-dot{
        width: .32rem;
        height: .32rem;
        position: relative;
        display: inline-block;
        border-radius: 50%;
        background-color: #2d8cf0;
        -webkit-animation: ani-spin-bounce 1s 0s ease-in-out infinite;
        animation: ani-spin-bounce 1s 0s ease-in-out infinite;
      }
      .ivu-spin-text{
        margin-top: -.2rem;
        color: #2d8cf0;
        font-size: .14rem;
      }
    }
  }
</style>
