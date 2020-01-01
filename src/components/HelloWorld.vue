<template>
  <div class="container">
    <div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
      <ol class="carousel-indicators">
        <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
        <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
        <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
      </ol>
      <div class="carousel-inner">
        <div class="carousel-item active">
          <img src="https://akcdn.detik.net.id/community/media/visual/2019/12/12/3968ba26-1514-40d2-b7e4-36720f6f1abe_169.jpeg?w=700&q=80" class="d-block w-100" alt="...">
        </div>
        <div class="carousel-item">
          <img src="https://akcdn.detik.net.id/community/media/visual/2019/12/23/8f53eade-8cc0-46c6-a238-66383eb1eab6_169.jpeg?w=700&q=80" class="d-block w-100" alt="...">
        </div>
        <div class="carousel-item">
          <img src="https://akcdn.detik.net.id/community/media/visual/2019/12/23/52811af3-ae4f-4ba6-ab48-9df4eb61c8d9_169.jpeg?w=700&q=80" class="d-block w-100" alt="...">
        </div>
      </div>
      <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
      </a>
      <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  
}
</script>

<style scoped>
  #carouselExampleIndicators{
    margin-top: 5px;
  }
</style>