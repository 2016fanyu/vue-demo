<template>
  <el-container class="container">
    <el-aside style="width: 230px">
      <el-col>
        <el-menu
          default-active="2"
          class="el-menu-vertical-demo"
          @open="handleOpen"
          @close="handleClose"
          background-color="#91a17d"
          text-color="#fff">
          <el-submenu index="1">
            <template slot="title">
              <i class="el-icon-menu"></i>
              <span>导航一</span>
            </template>
            <el-menu-item index="1-1">选项1</el-menu-item>
            <el-menu-item index="1-2">选项2</el-menu-item>
            <el-menu-item index="1-3">选项3</el-menu-item>
          </el-submenu>
          <el-submenu index="2">
            <template slot="title">
              <i class="el-icon-menu"></i>
              <span>导航二</span>
            </template>
            <el-menu-item index="2-1">选项1</el-menu-item>
            <el-menu-item index="2-2">选项2</el-menu-item>
          </el-submenu>
          <el-submenu index="3">
            <template slot="title">
              <i class="el-icon-menu"></i>
              <span>导航三</span>
            </template>
            <el-menu-item index="3-1">选项1</el-menu-item>
          </el-submenu>
        </el-menu>
      </el-col>
    </el-aside>
    <el-main>
      <el-breadcrumb separator-class="el-icon-arrow-right">
        <el-breadcrumb-item :to="{ path: '/' }">首页</el-breadcrumb-item>
        <el-breadcrumb-item>活动管理</el-breadcrumb-item>
        <el-breadcrumb-item>活动列表</el-breadcrumb-item>
        <el-breadcrumb-item>活动详情</el-breadcrumb-item>
      </el-breadcrumb>
      <el-row>
        <el-col class="title">
          jQuery([selector,[context]])
          <span>返回值:Boolean</span>
        </el-col>
        <el-col class="summary">
          概述
        </el-col>
        <el-col class="summary_content">
          <p>内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内</p>
          <p>属性值。引号在大多数情况下是可选的。但在遇到诸如属性值包含"]"时，用以避免冲突。</p>
          <p>容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内</p>
          <p>容内容内容内容内容内容内容内容内容内容</p>
        </el-col>
        <el-col class="summary">
          参数
        </el-col>
        <el-col class="summary_param">
          <div class="clearfix">
            <span>value</span>
            <span>String</span>
            <span>v1.0</span>
          </div>
          <div>
            属性值。引号在大多数情况下是可选的。但在遇到诸如属性值包含"]"时，用以避免冲突。
          </div>
        </el-col>
        <el-col class="summary_param">
          <div class="clearfix">
            <span>value</span>
            <span>String</span>
            <span>v1.0</span>
          </div>
          <div>
            属性值。引号在大多数情况下是可选的。但在遇到诸如属性值包含"]"时，用以避免冲突。
          </div>
        </el-col>
        <el-col class="summary">
          示例
        </el-col>
        <el-col class="summary_eg">
          <div class="summary_eg_summary">描述</div>
          <div>匹配表单中所有的子级input元素</div>
          <div class="summary_eg_title">html代码</div>
          <div class="summary_eg_block">2222</div>
          <div class="summary_eg_title">jquery代码</div>
          <div class="summary_eg_block">2222</div>
          <div class="summary_eg_title">结果</div>
          <div class="summary_eg_block">222</div>
        </el-col>
      </el-row>
    </el-main>
  </el-container>
</template>

<script>
export default {
  methods: {
    handleOpen (key, keyPath) {
      console.log(key, keyPath)
    },
    handleClose (key, keyPath) {
      console.log(key, keyPath)
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "./style/style";
  .container {
    height: 100%;
    .el-aside {
      background: $color-primary;
      .el-submenu {
        width: 230px;
      }
      .el-menu-vertical-demo{
        height: 100%
      }
      .el-submenu__title i{
        color: #fff;
      }
      .el-menu-item.is-active{
        color: #374b1e;
        border-left: 6px solid #374b1e;
      }
      .el-menu-item:hover{
        border-left: 6px solid #628634;
      }
    }
  }
  .el-main {
    background-color: #dde2d7;
    color: #333;
    .el-col.title{
      margin-top: 10px;
      padding: 0 10px;
      background: #374b1e;
      color: #fff;
      line-height: 36px;
      span{
        display: inline-block;
        float: right;
      }
    }
    .el-col.summary{
      margin-top: 10px;
      padding: 0 10px;
      background: #91a17d;
      color: #fff;
      line-height: 30px;
    }
    .el-col.summary_content{
      font-size: 14px;
      padding: 10px;
      text-indent: 2em;
      p{
        line-height: 18px;
        margin: 8px 0;
      }
    }
    .summary_param{
      font-size: 14px;
      padding: 0 10px;
      div{
        margin-top: 5px;
        line-height: 30px;
      }
      div:first-child{
        border-bottom: 1px solid #ccc;
        span{
          display: inline-block;
          width: 33%;
          float: left;
          font-weight: bold;
          &:last-child{
            color: #aaa;
          }
        }
      }
    }
    .summary_eg{
      font-size: 14px;
      div{
        margin: 10px 0;
      }
      .summary_eg_summary{
        padding-left: 8px;
        border-left: 4px solid $color-primary;
      }
      .summary_eg_title{
        color: #54752c;
      }
      .summary_eg_block{
        border: 1px dotted #54752c;
        padding: 10px;
      }
    }
    
  }
  
  body > .el-container {
    margin-bottom: 40px;
  }
  
  .el-container:nth-child(5) .el-aside,
  .el-container:nth-child(6) .el-aside {
    line-height: 260px;
  }
  
  .el-container:nth-child(7) .el-aside {
    line-height: 320px;
  }
</style>
