<template>
 
 <div class="main-banner" id="top">
        <div class="container-fluid">
          <div class="row">
            <div class="col-lg-6">
              <div class="left-content">
                <div class="thumb">
                  <div class="inner-content">
                    <h4>Top hit 100</h4>

                    <div class="main-border-button">
                      <a href="#">Xem ngay</a>
                    </div>
                  </div>
                  <img  class="mt-2" style="width: 100%;" src="https://focusevent.vn/wp-content/uploads/2020/12/photo-11.jpg">
                </div>
              </div>
            </div>
            <div class="col-lg-3">

              <div class="right-content">
                <div class="row">
                  <div class="col-lg-12">
                    <div class="right-first-image">
                    <div class="thumb">
                  <div class="inner-content">
                   <h5> <strong style="color: white;">Đưa âm nhạc của bạn đến gần hơn với mọi người</strong></h5>

                    <div class="main-border-button mt-2">
                      <a href="#">Tại đây</a>
                    </div>
                  </div>
                  <img  class="mt-2"  src="https://ss-images.saostar.vn/pc/1663294672127/saostar-3xewuuj7qxn73ehk.jpg">
                </div>
                    </div>
                  </div>

                  <div class="col-lg-12">
                    <div class="right-first-image">
                    <div class="thumb">
                  <div class="inner-content">
                    <h4>Top thịnh hành</h4>

                    <div class="main-border-button">
                      <a href="#">Xem ngay</a>
                    </div>
                  </div>
                  <img  class="mt-2"  src="https://vn.blog.kkday.com/wp-content/uploads/danny-howe-bn-D2bCvpik-unsplash.jpg">
                </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="col-lg-3">
              
              <div class="right-content">
                <div class="row" v-if="categories && categories.length">
                  <div class="col-lg-12" v-for="category in categories" :key="category.id">
                  <div class="inner-content " style="background: #000;">
                    <div class="main-border-button mt-2 " :style="getBackgroundStyle(category.linkBackGround) " style="position: relative; height: 96px;  background-size: cover;  background-position: center center; " >
                      <a href="#" class="mt-4"  style="z-index: 2;">{{category.nameCategory}}</a>
                    </div>
                  </div>
                
                </div>
                <div v-if="error">{{ error }}</div>
                <!-- <div class="col-lg-12">
                  <div class="inner-content " style="background: #000;">
                    <div class="main-border-button mt-2 " style="position: relative; height: 96px; background-size: cover;  background-position: center center;  background-image: url(https://toigingiuvedep.vn/wp-content/uploads/2021/10/hinh-anh-chill-dep-buon-cham-toi-trai-tim-bao-nguoi-2.jpg);">
                   
                      <a href="#" class="mt-4"  style="z-index: 2;">LO-FI</a>
                    </div>
                  </div>
                
                </div>
                <div class="col-lg-12">
                  <div class="inner-content " style="background: #000;">
                    <div class="main-border-button mt-2 " style="position: relative; height: 96px; background-size: cover;  background-position: center center;  background-image: url(https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRNZLhDJfitlsZGSLSQuCpzK2i6gMMVHXUhK8ZmePMNTgGR7I50XGa3sq7yv7F8Uc233Zs&usqp=CAU);">
                   
                      <a href="#" class="mt-4"  style="z-index: 2;">Rap Hip Hop</a>
                    </div>
                  </div>
                
                </div>
                <div class="col-lg-12">
                  <div class="inner-content " style="background: #000;">
                    <div class="main-border-button mt-2 " style="position: relative; height: 96px; background-size: cover;  background-position: center center;  background-image: url(https://cdn.tgdd.vn/Files/2021/08/23/1377229/nhac-ballad-la-gi-nguon-goc-va-dac-diem-noi-bat-c-2.jpg);">
                   
                      <a href="#" class="mt-4"  style="z-index: 2;">Ballad</a>
                    </div>
                  </div>
                
                </div>
                <div class="col-lg-12">
                  <div class="inner-content " style="background: #000;">
                    <div class="main-border-button mt-2 " style="position: relative; height: 96px; background-size: cover;  background-position: center center;  background-image: url(https://www.taylorguitars.com/sites/default/files/styles/hero_rotator_image/public/images/2022-09/HGG-2-2250x762_0.jpg?itok=TOLcCMk3);">
                   
                      <a href="#" class="mt-4"  style="z-index: 2;">Acoustic Guitars</a>
                    </div>
                  </div>
                
                </div>
                    
                <div class="col-lg-12">
                  <div class="inner-content " style="background: #000;">
                    <div class="main-border-button mt-2 " style="position: relative; height: 96px; background-size: cover;  background-position: center center;  background-image: url(https://media.graphassets.com/XrgacrQwKVeqJ1HyE8wg);">
                   
                      <a href="#" class="mt-4"   style="z-index: 2;">BEAT</a>
                    </div>
                  </div>
                
                </div> -->

                 
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

</template>

<script>
import axios from 'axios'

export default {
  data() {
    return {
      categories: []
    };
  },
  created() {
    this.getCate();
  },
  
  methods: {
    getCate() {
      axios.get('http://localhost:9090/api/getCate')
        .then(response => {
          console.log("response.data "+ response.data.data)
          this.categories = response.data.data;
        })
        .catch(error => {
          console.error(error);
        });
    },
    getBackgroundStyle(url) {
      return `background-image: url(${url})`;
    }
  }
};
</script>
<!-- <script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script> -->
