<template>
<div class="background">
  <div class="topbar"></div>
  <div class="topcolor">
    <div class="dropdowns">
      <el-dropdown>
        <span class="el-dropdown-link">
          最新消息
        </span>
      </el-dropdown>
      <el-dropdown>
        <span class="el-dropdown-link">
          招生<i class="el-icon-s-custom el-icon--left"></i>
        </span>
        <el-dropdown-menu slot="dropdown">
          <el-dropdown-item>春之清華卓越獎學金</el-dropdown-item>
          <el-dropdown-item>FB粉絲專頁</el-dropdown-item>
          <el-dropdown-item>2020招生</el-dropdown-item>
          <el-dropdown-item>招生Q&A</el-dropdown-item>
          <el-dropdown-item>過往招生資訊</el-dropdown-item>
        </el-dropdown-menu>
      </el-dropdown>
      <el-dropdown>
        <span class="el-dropdown-link">
          關於科藝組<i class="el-icon-more el-icon--left"></i>
        </span>
        <el-dropdown-menu slot="dropdown">
          <el-dropdown-item>科藝組簡介</el-dropdown-item>
          <el-dropdown-item>科藝組課程</el-dropdown-item>
          <el-dropdown-item>國際交換</el-dropdown-item>
          <el-dropdown-item>未來新建案</el-dropdown-item>
          <el-dropdown-item>師資</el-dropdown-item>
        </el-dropdown-menu>
      </el-dropdown>
      <el-dropdown>
        <span class="el-dropdown-link">
          作品賞析<i class="el-icon-menu el-icon--right"></i>
        </span>
        <el-dropdown-menu slot="dropdown">
          <el-dropdown-item>導師作品</el-dropdown-item>
          <el-dropdown-item>學生作品</el-dropdown-item>
          <el-dropdown-item>數位文創作品</el-dropdown-item>
          <el-dropdown-item>互動藝術作品</el-dropdown-item>
          <el-dropdown-item>動力藝術作品</el-dropdown-item>
          <el-dropdown-item>聲音藝術作品</el-dropdown-item>
          <el-dropdown-item>科技表演作品</el-dropdown-item>
        </el-dropdown-menu>
      </el-dropdown>
      <el-dropdown>
        <span class="el-dropdown-link">
          聯絡我們<i class="el-icon-phone-outline el-icon--right"></i>
        </span>
      </el-dropdown>
    </div>
  </div>
  <div class="topbar"></div>
  <!-- <div class="pictures">
    <img src="~@/assets/" >
  </div> -->
</div>
</template>

<script>

</script>

<style>
html,
body{
  padding: 0;
  margin: 0;
}
.topbar{
  height: 20px;
  background-color: rgb(33, 37, 21);
}
.background{

  background-image:url('~@/assets/sunset.jpg');
  width: 100vw;
  height:100vmax;
  margin: 0%;
  padding: 0%;
  opacity: 0.79;
}
.dropdowns{
  display: flex;
  justify-content: space-evenly;
  top: 50px;
  background-color: rgb(33, 37, 21);
}
.el-dropdown-link {
    opacity: 0.7;
    cursor:pointer;
    color:rgb(255, 217, 226);
    font-size: 17px;
    font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
	}
.el-dropdown-link:hover{

  opacity: 1;

}
.el-icon-arrow-down {
  font-size: 17px;
}



</style>
