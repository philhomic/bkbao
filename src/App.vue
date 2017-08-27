<template>
  <v-app id="example-3" toolbar>
    <v-toolbar fixed>
      <v-toolbar-title class="toolbar-title">
        <!--<img src="./assets/img/treasure.png" alt="" class="logo">-->
        BKBao — 备课宝
        <span class="remark"> [兼容PowerPoint 2010以上版本] </span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn large flat>我们的愿景</v-btn>
        <v-btn large flat>功能教程</v-btn>
        <v-btn large flat>常见问题</v-btn>
        <v-btn large flat class="last-nav-btn">关于我们</v-btn>
      </v-toolbar-items>
    </v-toolbar>
    <main>
      <img width="100%" src="./assets/img/screenshot.png" alt="">
      <div class="hope">
        <img src="./assets/img/graffiti.jpg" alt="">
        <div class="mask">用PPT做课件<br>简单得<b>不要不要</b>的</div>
        <h2 class="hope-text">— 我们的愿景 —</h2>
        <p class="download-btn-wrapper">
          <button class="download-btn">免费下载</button>
        </p>
      </div>

      <div class="tutorial-section">
        <v-container>
          <!--v-router-->
          <v-layout>
            <h2 class="tutorial-title">— 功能教程 —</h2>
          </v-layout>
          <v-layout row-sm column child-flex-sm>
            <v-card class="ma-2 tutorial">
              <v-card-media>
                <iframe frameborder="0" src="https://v.qq.com/iframe/player.html?vid=m0024nvac3j&tiny=0&auto=0"
                        allowfullscreen></iframe>
              </v-card-media>
              <v-card-text>录入习题<br>改为遮罩填空题、添加注释框</v-card-text>
            </v-card>
            <v-card class="ma-2 tutorial">
              <v-card-media>
                <iframe frameborder="0" src="https://v.qq.com/iframe/player.html?vid=m0024nvac3j&tiny=0&auto=0"
                        allowfullscreen></iframe>
              </v-card-media>
              <v-card-text>添加动画效果<br>点A显B、点A隐B</v-card-text>
            </v-card>
            <v-card class="ma-2 tutorial">
              <v-card-media>
                <iframe frameborder="0" src="https://v.qq.com/iframe/player.html?vid=m0024nvac3j&tiny=0&auto=0"
                        allowfullscreen></iframe>
              </v-card-media>
              <v-card-text>☆ PPT课件的三种模式<br>基础设置、设置默认样式</v-card-text>
            </v-card>
          </v-layout>
          <v-layout row-sm column child-flex-sm>
            <v-card class="ma-2 tutorial">
              <v-card-media>
                <iframe frameborder="0" src="https://v.qq.com/iframe/player.html?vid=m0024nvac3j&tiny=0&auto=0"
                        allowfullscreen></iframe>
              </v-card-media>
              <v-card-text>新建页面内容、添加链接页面</v-card-text>
            </v-card>
            <v-card class="ma-2 tutorial">
              <v-card-media>
                <iframe frameborder="0" src="https://v.qq.com/iframe/player.html?vid=m0024nvac3j&tiny=0&auto=0"
                        allowfullscreen></iframe>
              </v-card-media>
              <v-card-text>批量生成PPT、批量分割PPT</v-card-text>
            </v-card>
            <v-card class="ma-2 tutorial">
              <v-card-media>
                <iframe frameborder="0" src="https://v.qq.com/iframe/player.html?vid=m0024nvac3j&tiny=0&auto=0"
                        allowfullscreen></iframe>
              </v-card-media>
              <v-card-text>批量添加音频媒体</v-card-text>
            </v-card>
          </v-layout>
        </v-container>
      </div>

      <div class="divider"></div>
      <div class="question-section">
        <v-container>
          <v-layout>
            <h2 class="question-title">— 常见问题 —</h2>
          </v-layout>
          <v-expansion-panel class="question-panel" v-for="(item, i) in questions" :key="i">
            <v-expansion-panel-content>
              <div class="question" slot="header">{{i + 1}}. {{item[0]}}</div>
              <v-card>
                <v-card-text class="grey lighten-3 answer">{{item[1]}}</v-card-text>
              </v-card>
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-container>
      </div>

      <div class="divider"></div>
      <div class="about-section">
        <v-container>
          <v-layout>
            <h1 class="about-title">— 关于我们 —</h1>
          </v-layout>
        </v-container>
      </div>
    </main>
  </v-app>
</template>

<script type="text/ecmascript-6">
  export default {
    name: 'app',
    data () {
      return {
        questions: [
            ['为什么我总是安装不成功', '该插件依赖于 .NET 4.0 的环境，因此要确保您的电脑上已经安装有此环境。如果没有的话，请到****这个网址下载安装。'],
            ['为什么我添加上去的按钮，不点击也能播放动画效果？', '请仔细看第**个视频教程。如果您希望一定是点击按钮才播放动画，而不是随意单击就播放的话，请确保插件中左侧第一个PPT模式的选择中，您选择的是"按钮动画"。']
        ]
      }
    }
  };
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
  @import 'assets/stylus/style.css'
  .toolbar-title
    .logo
      //display: inline-block
      vertical-align: middle
      width: 40px
      height: 30px
      margin-right: 10px
    .remark
      font-size: 14px

  .last-nav-btn
    margin-right: 40px

  .hope
    position: relative
    height: 20em
    overflow: hidden
    .hope-text
      position: absolute
      top: 20px
      width: 100%
      color: #fff
      line-height: 2em
      font-size: 1.8em
      text-align: center
      text-shadow: 5px 5px 5px #000000
    .mask
      position: absolute
      top: 0
      left: 0
      right: 0
      bottom: 0
      padding-top: 60px
      background-color: rgba(0, 0, 0, 0.6)
      /*line-height: 340px*/
      text-align: center
      color: #fff
      font-size: 3em
      font-weight: 800
      font-family: Helvetica, 'Hiragino Sans GB', 'Microsoft Yahei', '微软雅黑', Arial, sans-serif;
      text-shadow: 5px 5px 5px #000000
    .download-btn-wrapper
      position: absolute
      width: 100%
      bottom: 0
      text-align: center
      button
        display: inline-block
        font-size: 1.5em
        font-weight: 700
        color: #fff
        background-color: rgba(204, 75, 75, 1)
        padding: 10px 20px
        border-radius: 5px
        font-family: Helvetica, 'Hiragino Sans GB', 'Microsoft Yahei', '微软雅黑', Arial, sans-serif;

  .tutorial-title, .question-title, .about-title
    width: 100%
    line-height: 2em
    font-size: 1.8em
    font-weight: 700
    text-align: center
    text-shadow: 5px 5px 5px #ddd

  .tutorial
    text-align: center
    padding-top: 10px

  .divider
    width: 100%
    border-bottom: 1px solid #ddd

  .question-section
    background-color: rgba(243, 247, 250, 1)
    padding-bottom: 30px

  .question
    font-size: 1em
    font-family: Helvetica, 'Hiragino Sans GB', 'Microsoft Yahei', '微软雅黑', Arial, sans-serif;
    font-weight: 600

  .question-panel
    box-shadow: none
    background-color: #FFF

</style>
