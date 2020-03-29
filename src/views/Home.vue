<template>
  <div class="home">
    <!--슬라이드1-->
    <el-carousel :interval="5000" arrow="always" style="height:360px;">
      <el-carousel-item v-for="item in carouselData" :key="item" style="height:360px;">
        <img class="carousel-item-img" :src="item.imageUrl" alt="" height="400">
      </el-carousel-item>
    </el-carousel>
    
    <!-- <section>
      <div v-for="item in tripData" :key="item.id">
        <Trip :trip='item'> </Trip>
      </div>
    </section> -->
    
    <!--key : 잘돌아가기위한-->


  <!--tab-->
  <section style="height:400px;">
  <h3>지금 인기있는 여행지</h3>

  <el-tabs :tab-position="tabPosition" id="nav_tab">

    <el-tab-pane label="오사카" class="popular"> 
      <div v-for="item in Osaka" :key="item.id">
        <Trip :trip='item'></Trip>
      </div>
    </el-tab-pane>
    <el-tab-pane label="싱가포르" class="popular">
      <div v-for="item in singapore" :key="item.id">
        <Trip :trip='item'></Trip>
      </div>
    </el-tab-pane>
    <el-tab-pane label="파리" class="popular">
      <div v-for="item in paris" :key="item.id">
        <Trip :trip='item'></Trip>
      </div></el-tab-pane>
    <el-tab-pane label="홍콩" class="popular">
      <div v-for="item in hongkong" :key="item.id">
        <Trip :trip='item'></Trip>
      </div></el-tab-pane>
    <el-tab-pane label="런던" class="popular">
      <div v-for="item in london" :key="item.id">
        <Trip :trip='item'></Trip>
      </div></el-tab-pane>
    <!-- <el-tab-pane label="도쿄">도쿄</el-tab-pane>
    <el-tab-pane label="타이페이">타이페이</el-tab-pane>  
    <el-tab-pane label="파리">파리</el-tab-pane>  -->
  </el-tabs>
  </section>

  <!--테마-->
  <section>
    <h3>테마가 있는 여행</h3>
    <ul id="theme">
      <li>
        <img src="https://d2ur7st6jjikze.cloudfront.net/themes/447_mobile_medium_1545891243.jpg?1545891243" width="340" height="180" alt="">
        <p class="title1">몬세라트-시체스</p>
        <p>일일, 반일 및 소수정예 모두 OK!</p>
      </li>
       <li>
        <img src="https://d2ur7st6jjikze.cloudfront.net/offer_photos/41080/258555_medium_1535619221.jpg?1535619221" width="340" height="180" alt="">
        <p class="title1">가오슝 가슝?</p>
        <p>대만 남부 파헤치기~ 가오슝, 아리산, 타이중</p>
      </li>
       <li>
        <img src="https://d2ur7st6jjikze.cloudfront.net/themes/389_mobile_medium_1525740787.jpg?1525740787" width="340" height="180" alt="">
        <p class="title1">버스타고 오사카</p>
        <p>안전은 기본, 합리적인 가격까지!</p>
      </li>
    </ul>
  </section>

  <!--슬라이드2-->
  <el-carousel :interval="5000" arrow="always" style="height:360px;">
      <el-carousel-item v-for="item in carousel2Data" :key="item" style="height:360px;">
        <img :src="item.imageUrl" alt="" width="100%" height="400">
      </el-carousel-item>
    </el-carousel>


  <!--버튼-->
  <section>
    <div id="checklist">
      <div></div>
       <h2>안챙기면 후회하는 여행 전 필수 체크리스트</h2>
       <p>포켓 와이파이, 환전, 면세점, 여행자보험, 렌터카. 미리미리 알뜰하게 준비하세요!</p>
       <button>확인하러 가기</button>
    </div>
  </section>
  


  </div>
</template>



<script>
import Trip from '../components/trip.vue'
// @ is an alias to /src

export default {
  name: 'home',
  components: {
    Trip
  },

  
  data(){ //데이터 저장소
    return {

      carouselData: [
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/cms/478_original_1543567760.jpg?1543567760',
          id: 1
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/cms/624_original_1548723278.jpg?1548723278',
          id: 2
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/cms/550_original_1548742469.jpg?1548742469',
          id: 3
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/cms/618_original_1548225460.jpg?1548225460',
          id: 4
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/cms/618_original_1548225460.jpg?1548225460',
          id: 5
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/cms/601_original_1546506536.jpg?1546506536',
          id: 6
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/cms/49_original_1525398868.jpg?1525398868',
          id: 7
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/cms/51_original_1525398977.jpg?1525398977',
          id:8
        }

      ],


      Osaka: [
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/offer_photos/5554/26990_medium_1525339431.jpg?1525339431',
          id: 1,
          tip: '티켓/쿄통패스·오사카',
          title: '[무료배송] 오사카 라피트 왕복권 (교환권)',
          price:'20,600원'
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/offer_photos/17958/110355_medium_1525746431.jpg?1525746431',
          id: 2,
          tip: '티켓/쿄통패스·오사카',
          title: '★[전공항] 일본 플레이와이파이 포켓와이파이 무제한 데이터  + 보조배터리 + 안심보험 ★',
          price:'20,600원'
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/offer_photos/4031/18202_medium_1526008073.jpg?1526008073',
          id: 3,
          tip: '티켓/쿄통패스·오사카',
          title: '[무료배송] 오사카 주유패스 2일권',
          price:'20,600원'
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/offer_photos/22565/147564_medium_1525760159.jpg?1525760159',
          id: 4,
          tip: '티켓/쿄통패스·오사카',
          title: '[인천/김포/김해공항 수령] 오사카 라피트 왕복권 (교환권)',
          price:'20,600원'
        }
      ],

      singapore: [
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/offer_photos/21988/133661_medium_1525762500.jpg?1525762500',
          id: 1,
          tip: '티켓/쿄통패스·싱가포르',
          title: '[모바일 제시가능] 싱가포르(싱가폴) 유니버셜 스튜디오 입장권 e티켓',
          price:'20,600원'
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/offer_photos/11748/73779_medium_1525778821.jpg?1525778821',
          id: 2,
          tip: '티켓/쿄통패스·싱가포르',
          title: '싱가포르(싱가폴) 루지 탑승권/스카이 라이드 티켓 - 옵션확인필수',
          price:'20,600원'
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/offer_photos/25062/153267_medium_1525767960.jpg?1525767960',
          id: 3,
          tip: '티켓/쿄통패스·싱가포르',
          title: '싱가포르(싱가폴) 가든스 바이 더 베이 입장권 e티켓',
          price:'20,600원'
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/offer_photos/26448/163015_medium_1525770599.jpg?1525770599',
          id: 4,
          tip: '티켓/쿄통패스·싱가포르',
          title: '싱가포르(싱가폴) 리버 크루즈 티켓',
          price:'20,600원'
        }
      ],

         paris: [
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/offer_photos/7366/40188_medium_1525763659.jpg?1525763659',
          id: 1,
          tip: '티켓/쿄통패스·파리',
          title: '파리 1일 완성(몽마르트 포함) 워킹투어 (신청시 몽생미셸 투어 1인 85,000원 제공)',
          price:'20,600원'
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/offer_photos/5047/23871_medium_1525259121.jpg?1525259121',
          id: 2,
          tip: '티켓/쿄통패스·파리',
          title: '파리 바토무슈 E-티켓(바코드) [교환없이 즉시 탑승]',
          price:'20,600원'
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/offer_photos/2654/11109_medium_1525780835.jpg?1525780835',
          id: 3,
          tip: '티켓/쿄통패스·파리',
          title: '[종합후기4.8/업계1위] 몽생미셸S야경투어(숙소샌딩/샌드위치/워킹제공) *고객만족1위수상',
          price:'20,600원'
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/offer_photos/10322/66609_medium_1525744495.jpg?1525744495',
          id: 4,
          tip: '티켓/쿄통패스·파리',
          title: '[핵심쏙쏙] A Tale of the Louvre, 루브르 감감 (監感) 투어 *200分*',
          price:'20,600원'
        }
      ],

      hongkong: [
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/offer_photos/15441/194552_medium_1525743333.jpg?1525743333',
          id: 1,
          tip: '티켓/쿄통패스·홍콩',
          title: '[모바일 제시가능]홍콩 디즈니랜드 입장권 e티켓',
          price:'20,600원'
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/offer_photos/16023/97151_medium_1525743035.jpg?1525743035',
          id: 2,
          tip: '티켓/쿄통패스·홍콩',
          title: '홍콩 : AEL 티켓 (QR코드 바로 탑승)',
          price:'20,600원'
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/offer_photos/15737/95234_medium_1525779074.jpg?1525779074',
          id: 3,
          tip: '티켓/쿄통패스·홍콩',
          title: '[홍콩 공항 수령] 옥토퍼스 카드 성인 - HK$50 기본제공',
          price:'20,600원'
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/offer_photos/29310/184016_medium_1525760517.jpg?1525760517',
          id: 4,
          tip: '티켓/쿄통패스·홍콩',
          title: '[모바일 제시가능]홍콩 디즈니랜드 밀 쿠폰(식사쿠폰) 2 in 1 ',
          price:'20,600원'
        }
      ],

      london: [
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/offer_photos/11138/152890_medium_1525743547.jpg?1525743547',
          id: 1,
          tip: '가이드투어·런던',
          title: '#런던 후기1위 #와인 한잔과 인생샷이 함께하는 최소한의 로맨틱 템즈강 야경투어',
          price:'20,600원'
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/offer_photos/1829/38084_medium_1525259178.jpg?1525259178',
          id: 2,
          tip: '가이드투어·런던',
          title: '[사전예약/빠른입장]  코츠월드 + 옥스포드  # 만족도 1위 #  1+1 이벤트 ',
          price:'20,600원'
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/offer_photos/315/11104_medium_1525338697.jpg?1525338697',
          id: 3,
          tip: '가이드투어·런던',
          title: '런던의 과거와 현재를 탐방하는 시내 워킹투어',
          price:'20,600원'
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/offer_photos/1867/17748_medium_1525258248.jpg?1525258248',
          id: 4,
          tip: '가이드투어·런던',
          title: '#조기마감# "대영박물관 집중투어" 18점의 유물이 들려주는 인류문명사 !!',
          price:'20,600원'
        }
      ],

      carousel2Data: [
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/cms/129_original_1525398982.jpg?1525398982',
          id: 1
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/cms/624_original_1548723278.jpg?1548723278',
          id: 2
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/cms/550_original_1548742469.jpg?1548742469',
          id: 3
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/cms/618_original_1548225460.jpg?1548225460',
          id: 4
        },
        {
          imageUrl:'https://d2ur7st6jjikze.cloudfront.net/cms/618_original_1548225460.jpg?1548225460',
          id: 5
        }

      ]


    }
  }
}
</script>


<style lang="scss">

    #nav_tab {
      margin: 0 auto;
      height: 200px; 
      width:70%;
    }

    .popular{
      display: flex;
    }
    
    h3{
      font-weight: bold;
      margin: 90px 0 30px 230px;
      font-size: 20px;
    }


    #theme{
      display: flex;
      width: 70%;
      margin: 0 auto;
      height: 300px;
      margin-bottom: 50px;
    }

    #theme li {
      margin-right: 20px;
      list-style: none;
    }

    #theme li .title1 {
      font-weight: bold;
      margin: 20px 0 5px 0;
      font-size: 18px;
    }

    .carousel-item-img {
      object-fit: cover;
    }
    
    #checklist{
      text-align: center;
      margin-top: 100px; 
      height: 300px;
    }
    

    #checklist div{
      border-top:1px solid gainsboro; 
      margin: 0 auto;
      width: 154px; 
      margin-bottom: 30px;
    }

    #checklist h2 {
      font-weight: bold;
      font-size: 20px;
      margin-bottom: 15px;

    }

    #checklist p {
      font-size: 14px;
      margin-bottom: 30px;
      color: gray;
    }

    #checklist button{
      padding:10px 80px;
      background-color: #2b96ed;
      color:white;
      font-size: 18px;
      font-weight: bold;
      box-shadow: 0 1px 3px 0 rgba(0,0,0,0.3);
      outline: 0;
      border: 0;
      border-radius: 5px;
    }
  </style>
