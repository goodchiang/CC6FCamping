<template>
    <!-- header -->
    <header class="navbar-fixed-top">
        <nav>
            <ul>
                <li><a href="#about">Home</a></li>
                <li><a href="#about">關於</a></li>
                <li><a href="#experience">時間軸</a></li>
                <li><a href="#projects">紀錄</a></li>

            </ul>
        </nav>
    </header>
    <!-- ./header -->

    <!-- home -->
    <div class="section" id="home" data-stellar-background-ratio="0.5">
        <div class="container">
            <div class="disply-table">
                <div class="table-cell" data-aos="fade-up" data-aos-delay="0">
                    <h4>Ahmed Eissa</h4>
                    <h1>Ui &<br /> Ux Designer</h1>
                </div>
            </div>
        </div>
    </div>
    <!-- ./home -->
      <!-- about -->
    <div class="section" id="about">
        <div class="container">
            <div class="col-md-6" data-aos="fade-up">
                <h4>About</h4>
                <h1 class="size-50">關於我們</h1>
                <div class="h-50"></div>
                <p>在某大樓六樓一起工作的夥伴們，假日互相揪團，露營曬小孩</p>
                <p></p>
                <div class="h-50"></div> <img src="" width="230" alt="" />
                <div class="h-50"></div>
            </div>
            <div class="col-md-6 about-img-div">
                <div class="about-border" data-aos="fade-up" data-aos-delay=".5"></div>
                <img src="" width="400" class="img-responsive" alt="" align="right" data-aos="fade-right" data-aos-delay="0" />
            </div>
        </div>
    </div>
    <!-- ./about -->

    <!-- TimeLine  -->
    <div class="section" id="experience">
        <div class="container">
            <div class="col-md-12">
                <h4>Timeline</h4>
                <h1 class="size-50">時間軸</h1>
                <div class="h-50"></div>
            </div>
            <div class="col-md-12">
                <ul class="timeline">
                  <TimeLine v-for="record in records" :key="record.id" :time="record.time" :campSite="record.campsite"/>
                </ul>
            </div>
        </div>
    </div>
    <!-- ./TimeLine -->

    <!-- projects -->
    <div class="section" id="projects">
        <div class="container">
            <div class="col-md-12">
                <h4>03</h4>
                <h1 class="size-50">My <br /> Projects</h1> 
            </div>
            <!-- main container -->
            <div class="main-container portfolio-inner clearfix">
                <!-- portfolio div -->
                <div class="portfolio-div">
                    <div class="portfolio">
                        <!-- portfolio_filter -->
                        <!-- <div class="categories-grid wow fadeInLeft">
                            <nav class="categories">
                                <ul class="portfolio_filter">
                                    <li><a href="" class="active" data-filter="*">All</a></li>
                                    <li><a href="" data-filter=".photography">Photography</a></li>
                                    <li><a href="" data-filter=".logo">Logo</a></li>
                                    <li><a href="" data-filter=".graphics">Graphics</a></li>
                                    <li><a href="" data-filter=".ads">Advertising</a></li>
                                    <li><a href="" data-filter=".fashion">Fashion</a></li>
                                </ul>
                            </nav>
                        </div> -->
                        <!-- portfolio_filter -->
                        
                        <!-- portfolio_container -->
                        <div class="no-padding portfolio_container clearfix" data-aos="fade-up">              
                            <MyAlbum v-for="record in records" :key="record.id" :snapshot="record.snapshot" :campSite="record.campsite" />
                        </div>
                        <!-- end portfolio_container -->

                    </div><!-- portfolio -->
                </div><!-- end portfolio div -->
            </div><!-- end main container -->
        </div>
    </div>
    <!-- ./projects -->
    

</template>

<script>
import TimeLine from './components/TimeLine.vue';
import MyAlbum from './components/MyAlbum.vue';
import campRecords from './assets/records.json';

export default {
  name: 'App',
  components: { TimeLine, MyAlbum },
  data() {
    return {
      records: campRecords,

      time: "2000.01.01",
      campsite: "台北市",
      snapshot:'https://lh3.googleusercontent.com/pw/AJFCJaXbGckIOP7juJVIzRoM7sOfhYGn2RAqSbWHr9xKj8RyDy5XWla2pj0_aM-JRGUmo9RRp56c7fBVMuBIs_g7jPd4T9voiZUZfxy52s6MzEyUefFdK4jnT-KCQkWVSoPQNNYE0Gt1Idxn89V8ByL3TRWhUQ=w1117-h838-s-no?authuser=1'
    }
  },
}
</script>

<style src="@/assets/css/style.css"></style>
