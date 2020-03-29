

<template>

<div id="header">
   <div class="header-search">
    <img src="../assets/trip/logo.png" width="130" height="30">
    <div class="header-searchbar">
      <img class="header-icon" width="20" height="20" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAwCAYAAABXAvmHAAAAAXNSR0IArs4c6QAABD1JREFUaAXtWE9IVEEYn3kGpWSUQdTSLTpHmBD9gaC6JKiHMqIuRaAdXI3IlQraIkOtKFcopahLUFmCCXXq4EG7RIfO0S228GDRH7V/b/p+b3dmx3Vnd957u+hhF5aZN/N9v9/85s/35nuMlX/lGSjPQHkGFnMGeBjyeDzuJL/M7mCuaOJM1ArGIwQYAaZgLEltSWp7yxw+GllT+Zrs3TB8uXwDCaCBrPg8PRsVwj1DA12XCzi7jYimOHdurK+pTJD/XHZ/0GffAlraOg8Kzm4yITYGIuX8o8OdjsH+npFA/llO1gKEEPxUtOuKy9xz8zBoQLRVnjuO84L+H8Sq5Un082+/Iq7rbqJ/PW2jxmzBDnOu3kn0XOCc0yIG/1kJwOBb22OPqWzOUPEk4+Livl11D5qbm/9l2hfWhoeHK15NvDnOBL9Ep8M7I7DijD8ZTPQeCSPCSkBrW6x7/szzsWVrq47ejsd/LByuuaWzs7P66yx7SCIapBVWYnCg97x89lsWFODteSaeZoB5YijR2xF01rCaLdHYLRIRlZi0EoeGBvqeyWc/ZV4BiDbJ6Zn3mf3Lx2jwTUEHLweWFjGqVoLOUaSmanOQ6ORI0FwlQqU2+CS2TdjBgwcYqyvZMap5Bx4cHleuQRRoMwqg2XAQ55U/HVi/e1755qj09fV9RxCQXeACp3y2LY0OeMOqlxQtMaKNLaitnYdJ2LAHl/dWt3VO2xkF4HogsRDnC4VKaeunBCawlY/GqdoKVIwCCLhW+uIlJevFLnVsndOWxygAFzMJgjesrBe71LF1TlseowCKr0qAvB7Ygvqx07F1TlsMowBbgLB2K2dm1LuILol0lv39jAIIKRWjCQ8XM3+w9tY//1ZsUNaCfVJ1y4pRAE2GEoBbpSWebzMdW+e0BTIK8DKpNAquxLaAfu10bJ3TFscoAGmgBCHgRlyJ5XOxSmACW+FpnKqtQMUoADksna4pz5/uKt59vgCY3+5UjpDK7MAFTr8YxlkdHx8Xddt3O4KJ/SlQvm3vnp13Jycnf/slyWWP3GDuD0daWY1+SjMvX+/tnshlm6/NuAJwQgJOV0fvrkK3lQiSEVyF8wHa9AEjndikohtxeFw2zlk2eQXgfk4Z6+mMj2hAMhJGRDoXQEKjsjJwBMkFMC6r2SxlSklDeEdJ0tageYaVAMxaazT2iM7D4cxqhE/qFRZ37g/195wMIsJKAIggopifVTDzhLolrAhrAZKoGB+2sOfpc8pIS3vXPSbcExKbBViJvIdYAWsVfD1AAk5hL0bqU+8Jrd9UhS184AsMbBdsGwxa+ZAYiPITJHyvgCKjCnLYsB93vagUYiVCCdDFhKmHEbEkBEB8UBFLRkBQEUtKQBARS06ASQTnrH4oce0l+vWf7zCqO5eqnjPEloqslLjewY6ePdBCf9RLyVXGLs9AeQYWaQb+A3YfFqRyaHjmAAAAAElFTkSuQmCC" alt="검색"> 
      <input type="header-search" placeholder="여행지나 상품을 검색해보세요!"> 
    </div>
  </div>

  <div class="header-menu">
    <ul>
      <li>파트너 등록하기</li>
      <li>로그인</li>
      <li>회원가입</li>
    </ul>
  </div>
<hr>
  <div class="header-nav">
    <ul> 
      <li><a href="#">전체여행지</a></li>
      <li><a href="#">홈</a></li>
      <li><a href="#">투어&티켓</a></li>
      <li><a href="#">항공권</a></li>
      <li><a href="#">숙소</a></li>
      <li><a href="#">에어텔</a></li>
    </ul>
  </div>

 
</div>
   
                    
</template>


<script>
export default {
  name: 'header',
  components: {
  }
}
 
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

#header {
  padding-top: 20px;
  width: 70vw;
  margin: 0 auto;
  height: 120px;
}

.header-search {
  width: 50%;
}

.header-search img {
 float: left;
}

.header-search .header-searchbar {
  width: 250px;
  height: 40px;
  border: 1px solid #efefef;
  margin-left: 150px;
  
}
.header-search .header-searchbar img{
  padding: 10px 0 0 10px;
}
.header-search input {
  width: 210px;
  padding-top: 13px;
  border: 0;
  outline: none;
}

.header-menu ul {
  float: right;
  margin-top: -30px;
}

.header-menu ul li {
  display: inline;
  padding: 10px 20px;
  
}

.header-menu ul li:nth-last-child(1) {
  border: solid 1px rgb(66, 148, 255);
  border-radius: 3px;
  color: rgb(66, 148, 255);
}
.header-nav {
  width: 70vw;
}

.header-nav ul {
  text-align: center;
  float: left;
}

.header-nav ul li {
  display: inline;
  padding: 10px 20px;
  
}

.header-nav ul li a {
  text-decoration: none;
  color: black; 
}
.header-nav ul li a:hover {
  padding: 10px 0;
 border-bottom: 2px solid rgb(66, 148, 255);
}

hr{
  border: 0.5px solid #f3f3f3;
  margin-top: 20px;
}
</style>
