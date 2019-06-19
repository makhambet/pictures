<template>
  <div class="imgs">
    <div class="all">
      <div v-for="(img, i) in images" :key="i">
        <img @click="btn(i)" :src="img" alt="">
      </div>
      <!-- <img src="../assets/a.jpg" alt="">
      <img src="../assets/_Never_give_up_089778_.jpg" alt="">
      <img src="../assets/87832.jpg" alt="">
      <img src="../assets/164103355-bubble-wallpapers.jpg" alt="">
      <img src="../assets/a.jpg" alt="">
      <img src="../assets/light-bulb-mermaid-ant-ladybug-photoshop-digital-art.jpeg" alt="">
      <img src="../assets/maxresdefault.jpg" alt="">
      <img src="../assets/the_pursuit_of_happyness.jpg" alt=""> -->
    </div>
    <p>{{nmb + 1}}</p>
    <div class="pictures">
      <img :src="image" alt="">
    </div>
    
  </div>
</template>

<script>
  export default {
    data() {
      return {
        images: [
          'http://xomka.org/wp-content/uploads/2017/02/photoshop-3.jpg',
          'https://pp.userapi.com/c848632/v848632509/b717b/AGsV5fMOEyY.jpg',
          'https://www.adobe.com/content/dam/acom/en/products/photoshop/max2018/riverflow-ps-720x520-2.jpg/_jcr_content/renditions/cq5dam.mobile_640.640.462.jpg',
          'https://cms-assets.tutsplus.com/uploads/users/23/posts/26731/preview_image/best-photoshop-photo-effects-actions-creative.jpg',
          'http://www.poetryclub.com.ua/upload/poem_all/00305532.jpg',
          'https://wordstream-files-prod.s3.amazonaws.com/s3fs-public/styles/simple_image/public/images/learn-photoshop.jpg?6TjDAeK_yeSG_YSXjOPJQmz_TGhwhai3&itok=i9HKHHLz',
          'https://elements-cover-images-0.imgix.net/2f84fc17-890f-46bf-a708-5a730fa21071?auto=compress%2Cformat&fit=max&w=710&s=4d251e142f7ccdac066ec7491932c24c',
          'https://graphicriver.img.customer.envatousercontent.com/files/264349893/Dispersion_PreviewImage_8000.jpg?auto=compress%2Cformat&fit=crop&crop=top&w=590&h=590&s=cbbb2b3bb0c5939ac072a41753eae063'
        ],
        nmb: 0,
        image: 'http://xomka.org/wp-content/uploads/2017/02/photoshop-3.jpg'
      }
    },
    methods: {
      btn(id) {
        this.nmb = id,
        this.image = this.images[id]
      }
    },
  }
</script>

<style scoped>
  .imgs{
    width: 100%;
  }
  .all{
    display: flex;
    width: 95%;
    margin: 0 auto;
    overflow-x: scroll;
    white-space: nowrap;
  }
  .all img{
    width: 300px;
    height: 200px;
    cursor: pointer;
  }
  .pictures{
    width: 50%;
    margin: 0 auto; 
  }
  .pictures img{
    width: 100%;
  }
  @media (max-width: 768px){
    .pictures{
      width: 95%;
      margin: 0 auto; 
    }
  }
</style>