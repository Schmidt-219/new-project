<template>
<div class="background">
  <div class="logobar">
    <img src="~@/assets/清華科藝.png" class="logosize">
  </div>
  <el-menu
    :default-active="2"
    class="el-menu-demo menu"
    mode="horizontal"
    @select="handleSelect"
    background-color="rgb(33, 37, 21)"
    text-color="rgb(255, 217, 226)"
    active-text-color="#ffd04b"
    :unique-opened="true">
    <el-menu-item index="4"><a href="https://www.ele.me" target="_blank">最新消息</a></el-menu-item>
    <el-submenu :index="1">
      <template slot="title"><i class="el-icon-s-custom el-icon--left"></i>招生</template>
      <el-menu-item index="2-1">春之清華卓越獎學金</el-menu-item>
      <el-menu-item index="2-2">FB粉絲專頁</el-menu-item>
      <el-menu-item index="2-3">2020招生</el-menu-item>
      <el-menu-item index="2-4">招生QnA</el-menu-item>
      <el-menu-item index="2-5">過往招生資訊</el-menu-item>
    </el-submenu>
    <el-submenu :index="2">
      <template slot="title"><i class="el-icon-more el-icon--left"></i>關於科藝組</template>
      <el-menu-item index="2-1">科藝組簡介</el-menu-item>
      <el-menu-item index="2-2">科藝組課程</el-menu-item>
      <el-menu-item index="2-3">國際交換</el-menu-item>
      <el-menu-item index="2-4">未來新建案</el-menu-item>
      <el-menu-item index="2-5">師資</el-menu-item>
    </el-submenu>
    <el-submenu :index="3">
      <template slot="title"><i class="el-icon-menu el-icon--right"></i>作品賞析</template>
      <el-menu-item index="2-1">導師作品</el-menu-item>
      <el-menu-item index="2-2">學生作品</el-menu-item>
      <el-menu-item index="2-3">數位文創作品</el-menu-item>
      <el-menu-item index="2-4">互動藝術作品</el-menu-item>
      <el-menu-item index="2-5">動力藝術作品</el-menu-item>
      <el-menu-item index="2-6">聲音藝術作品</el-menu-item>
      <el-menu-item index="2-7">科技表演作品</el-menu-item>
    </el-submenu>
    <el-menu-item index="4"><a href="https://www.ele.me" target="_blank"><i class="el-icon-phone-outline el-icon--right"></i>聯絡我們</a></el-menu-item>
  </el-menu>

  <div class="titlefont block">
      <div class="innerfont">
        <br>
        <br>
        <br>
        <br>
        <p>清華是國際頂尖科技大學，加上合校後的藝術學院，具備發展「科技藝術」的卓越條件。</p>
        <p>我們號召臺灣年輕一代的科技藝術學者專家，我們規劃有科技藝術跨域特別課程，並與業界合作推出創意跨域專題。</p>
        <p class="titlefont">你，不需猶豫，歡迎你的加入!</p>
      </div>
    <div class="pictureboard">
      <div class="container">
        <br>
        <br>
        <br>
        <img src="http://ipta.nthu.edu.tw/wp-content/uploads/2019/02/ART-02.jpg" alt="logo" class="image" aria-setsize="">
        <div class="overlay">
          <div class="text"><i class="el-icon-position el-icon--left"></i>新大樓</div>
        </div>
      </div>
      <div class="container">
        <br>
        <br>
        <img src="https://ipta.nthu.edu.tw/wp-content/uploads/2020/10/banner.png" alt="logo" class="image" aria-setsize="">
        <div class="overlay">
          <div class="text"><i class="el-icon-position el-icon--left"></i>系展詳情</div>
        </div>
      </div>
      <div class="container">
        <br>
        <br>
        <br>
        <img src="data:image/jpeg;base64,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" alt="logo" class="image" aria-setsize="">
        <div class="overlay">
          <div class="text"><i class="el-icon-position el-icon--left"></i>邱教授</div>
        </div>
      </div>
    </div>

    <div class="pictureboard">
      <div class="container">
        <br>
        <br>
        <br>
        <img src="https://i.ytimg.com/vi/uYPMwdTx1-4/maxresdefault.jpg" alt="logo" class="image" aria-setsize="">
        <div class="overlay">
          <div class="text"><i class="el-icon-position el-icon--left"></i>陳主任</div>
        </div>
      </div>
      <div class="container">
        <br>
        <br>
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSmfFcfRF3ED-yIDwNHDpPcbwK-e8AUPFVy3Q&usqp=CAU" alt="logo" class="image" aria-setsize="">
        <div class="overlay">
          <div class="text"><i class="el-icon-position el-icon--left"></i>蔡奇宏</div>
        </div>
      </div>
      <div class="container">
        <br>
        <br>
        <br>
        <img src="data:image/jpeg;base64,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" alt="logo" class="image" aria-setsize="">
        <div class="overlay">
          <div class="text"><i class="el-icon-position el-icon--left"></i>陳依純</div>
        </div>
      </div>
    </div>
    <div class="coreability">
      <div class="tailfont">
        <br>
        <br>
        <br>
        <br>
        <p><i class="el-icon-check el-icon--left"></i>社會關懷與品格實踐能力</p> 
        <p><i class="el-icon-check el-icon--left"></i>美感認知與經典欣賞能力</p> 
      </div>
      <div class="tailfont">
        <br>
        <br>
        <br>
        <br>
        <p><i class="el-icon-check el-icon--left"></i>自然感知與創新發想能力</p> 
        <p><i class="el-icon-check el-icon--left"></i>邏輯思辨與語文溝通能力</p> 
      </div>
      <div class="tailfont">
        <br>
        <br>
        <br>
        <br>
        <p><i class="el-icon-check el-icon--left"></i>國際觀點與在地行動能力</p> 
        <p><i class="el-icon-check el-icon--left"></i>資訊掌握與科技應用能力</p> 
      </div>
    </div>
    <div class="sign">
      <img src="~@/assets/schmidt.png" alt="" height="30px">
    </div>
  </div>
</div>
</template>

<script>
export default {
    data() {
      return {
        activeIndex: '1',
        activeIndex2: '1'
      };
    },
    methods: {
      handleSelect(key, keyPath) {
        console.log(key, keyPath);
      }
    }
  }
</script>

<style>
html,
body{
  padding: 0;
  margin: 0;
}

.logobar{
  height: 120px;
  background-color: rgb(33, 37, 21);
}
.logosize{
  height: 80px;
  margin-top: 30px;
  margin-left:40%;
}
.menu{
  display: flex;
  justify-content: space-evenly;
}

.background{
  /* background-image:url('~@/assets/sunset.jpg'); */
  background-image:url('~@/assets/sunset.jpg');
  width: 100vw;
  height:100vmax;
  margin: 0%;
  padding: 0%;
  opacity: 0.95;
}
/* .dropdowns{
  display: flex;
  justify-content: space-evenly;
  top: 50px;
  background-color: rgb(33, 37, 21);
}

/* change */

.block{
  background-image: url('~@/assets/smoothbackground.jpg');
  width: 100%;
  height: 88%;
  opacity: 0.78;
  margin: 0%;
  padding: 0%;
}
.titlefont{
  font-size: 40px;
  text-align:center;
  color:rgb(255, 217, 226) ;
}
.innerfont{
  margin-top: 0px;
  font-size: 15px;
  text-align:center;
}
.pictureboard{
  margin-top: 1px;
  display: flex;
  justify-content: space-evenly;
  /* background-image: url('~@/assets/smoothbackground.jpg'); */
  opacity: 0.78;
}
.container {
  position: relative;
  width: 20%;
  height:20%;
}

.image {
  border-radius: 15px;
  display: block;
  width: 100%;
  max-height:100%;
}

.overlay {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  height: auto;
  width: 100%;
  opacity: 0;
  transition: .5s ease;
  background-image:url('~@/assets/smoothbackground.jpg');
  border-radius: 15px;
}

.container:hover .overlay {
  opacity: 0.9;
  box-shadow:2px 2px 2px 1px rgb(247, 220, 162) ;
}

.text {
  color: rgb(247, 220, 162);
  opacity: 1;
  font-size: 20px;
  position: absolute;
  top: 50%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  text-align: center;
}
.coreability{
  display: flex;
  justify-content: space-around;
}
.tailfont{
  font-size: 20px;
  color:rgb(255, 213, 96) ;
  opacity: 0.85;
}
.sign{
  position: fixed;
  bottom: 10px;
  right: 10px;
}
</style>
