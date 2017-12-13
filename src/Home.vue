<template>
  <mt-swipe :auto="0"  @change="handleChange">
    <mt-swipe-item>
      <div class="photo photo-animate"><img src="./assets/logo.jpg" alt=""></div>
      <div class="title photo-animate"><h2>前端工程师一枚</h2></div>
      <div class="name photo-animate"><h2>范瑜</h2></div>
    </mt-swipe-item>
    <mt-swipe-item>
      <div class="title photo-animate"><h1>基本信息</h1></div>
      <div class="illustration"><img src="./assets/information.png" alt=""></div>
      <div class="discription character-animate">
        <p><span>籍贯：</span>山西平遥</p>
        <p><span>现居地：</span>上海</p>
        <p><span>手机：</span>10000000000</p>
        <p><span>邮箱：</span>111111111@qq.com</p>
      </div>
    </mt-swipe-item>
    <mt-swipe-item>
      <div class="title photo-animate"><h1>工作经历</h1></div>
      <div class="illustration"><img src="./assets/work.png" alt=""></div>
      <div class="discription character-animate">
        <div class="one">
          <span>1</span>
          <div>
            <p>2016.07-2017.06</p>
            <p>上海XXXX公司</p>
          </div>
        </div>
        <div class="two">
          <span>2</span>
          <div>
            <p>2016.07-2017.06</p>
            <p>上海XXXX公司</p>
          </div>
        </div>
        <div class="three">
          <span>3</span>
          <div>
            <p>2016.07-2017.06</p>
            <p>上海XXXX公司</p>
          </div>
        </div>
      </div>
    </mt-swipe-item>
  </mt-swipe>
</template>

<script>
  import { Header, Swipe, SwipeItem } from 'mint-ui'
export default {
    component: {
      Header,
      Swipe,
      SwipeItem
    },
    methods: {
      handleChange (index) {
        console.log(index)
      }
    }
}
</script>

<style lang="scss" scoped>
  @import "./style/style";
  .mint-swipe-item {
    background: #00c4ff;
    &:first-child{
      background: url("./assets/bagOne.png") no-repeat;
      background-size: cover;
      .photo{
        width: 6rem;
        height: 6rem;
        margin: 0 auto;
        margin-top: 2rem;
        border-radius: 50%;
        overflow: hidden;
        img{
          width: 100%;
        }
      }
      .title {
        text-align: center;
        color: #fff;
      }
      .name {
        text-align: center;
        color: #fff;
      }
    }
    &:nth-child(2){
      background: #9260bf;
      .title{
        margin-top: 0;
        h1{
          text-align: center;
          color: #fff;
          font-weight: normal;
          font-size: 3rem;
        }
      }
      .discription{
        color: #fff;
        float: left;
        margin-top: 2rem;
        font-size: 1.2rem;
        min-width: 220px;
        margin-left: 50%;
        -webkit-transform: translateX(-50%);
        -moz-transform: translateX(-50%);
        -ms-transform: translateX(-50%);
        -o-transform: translateX(-50%);
        transform: translateX(-50%);
        span{
          color: #51207d;
        }
      }
    }
    &:nth-child(3){
      background: #ffbf51;
      .title{
        margin-top: 0;
        h1{
          text-align: center;
          color: #fff;
          font-weight: normal;
          font-size: 3rem;
        }
      }
      .discription{
        width: 90%;
        margin: 20px auto;
        &>div{
          border-left: 1px solid #e28100;
          height: 5rem;
          width: 50%;
          float: right;
          position: relative;
          p{
            padding: 0;
            margin: 0;
          }
          div{
            margin-top: -9px;
            padding: 0 1rem;
            color: #fff;
            font-size: 1rem;
          }
          span{
            display: inline-block;
            width: 18px;
            height: 18px;
            border-radius: 50%;
            text-align: center;
            line-height: 18px;
            color: #fff;
            background: #e28100;
            position: absolute;
            top: -9px;
            left: -9px;
          }
          &:nth-child(2){
            float: left;
            border-left: 0;
            text-align: right;
            -webkit-box-sizing: border-box;
            -moz-box-sizing: border-box;
            box-sizing: border-box;
            border-right: 1px solid #e28100;
            span{
              left: auto;
              right: -9px;
            }
          }
          &:last-child{
            border-left-color: #ffbf51;
          }
        }
      }
    }
    
    .illustration{
      width: 70%;
      margin: 0 auto;
      img{
        width: 100%;
      }
    }
    .photo-animate {
      -webkit-animation: topshow 1s linear;
      -o-animation: stopshow 1s linear;
      animation: topshow 1s linear;
    }
    .character-animate {
      -webkit-animation: bottomshow 1s linear;
      -o-animation: bottomshow 1s linear;
      animation: bottomshow 1s linear;
    }
    @keyframes topshow {
      0% {
        -webkit-transform: translateY(-10rem);
        -moz-transform: translateY(-10rem);
        -ms-transform: translateY(-10rem);
        -o-transform: translateY(-10rem);
        transform: translateY(-10rem);
        opacity: 0;
      }
      100% {
        -webkit-transform: translateX(0);
        -moz-transform: translateX(0);
        -ms-transform: translateX(0);
        -o-transform: translateX(0);
        transform: translateX(0);
        opacity: 1;
      }
    }
    @keyframes bottomshow {
      0% {
        opacity: 0;
      }
      100% {
        opacity: 1;
      }
    }
  }
</style>
