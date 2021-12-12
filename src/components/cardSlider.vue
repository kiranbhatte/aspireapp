<template>
  <div
    id="carouselExampleIndicators"
    class="carousel slide"
    data-bs-ride="carousel"
    ride="false"
  >
    <div class="carousel-indicators">
      <button
        type="button"
        data-bs-target="#carouselExampleIndicators"
        data-bs-slide-to="0"
        class="active"
        aria-current="true"
        aria-label="Slide 1"
      ></button>
      <button
        type="button"
        data-bs-target="#carouselExampleIndicators"
        data-bs-slide-to="1"
        aria-label="Slide 2"
      ></button>
      <button
        type="button"
        data-bs-target="#carouselExampleIndicators"
        data-bs-slide-to="2"
        aria-label="Slide 3"
      ></button>
    </div>
    <div class="carousel-inner">
      <div class="carousel-item active">
        <div class="aspirecard">
          <img alt="Vue logo" src="../assets/AspireWLogo.svg" class="pb-3"/>
          <p class="pb-3">Mark Henry</p>
          <p class="pb-2">1324 1235 4568 2020</p>
          <p>Thru: 12/20 <span>CVV: * * *</span></p>
          <img alt="Vue logo" src="../assets/VisaLogo.svg" />
        </div>
      </div>
      <div class="carousel-item">
        <div class="aspirecard">
          <img alt="Vue logo" src="../assets/AspireWLogo.svg" class="pb-3"/>
          <p class="pb-3">Mark Henry</p>
          <p class="pb-2">1324 1235 4568 2020</p>
          <p>Thru: 12/20 <span>CVV: * * *</span></p>
          <img alt="Vue logo" src="../assets/VisaLogo.svg" />
        </div>
      </div>
      <div class="carousel-item">
        <div class="aspirecard">
          <img alt="Vue logo" src="../assets/AspireWLogo.svg" class="pb-3"/>
          <p class="pb-3">Mark Henry</p>
          <p class="pb-2">1324 1235 4568 2020</p>
          <p>Thru: 12/20 <span>CVV: * * *</span></p>
          <img alt="Vue logo" src="../assets/VisaLogo.svg" />
        </div>
      </div>
    </div>
    <button
      class="carousel-control-prev"
      type="button"
      data-bs-target="#carouselExampleIndicators"
      data-bs-slide="prev"
    >
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button
      class="carousel-control-next"
      type="button"
      data-bs-target="#carouselExampleIndicators"
      data-bs-slide="next"
    >
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>
</template>
<script>
export default {
  name: "cardSlider"
};
</script>
<style scoped>
.aspirecard {
    background-color: #01D167;
    border-radius: 15px;
    padding: 25px 30px;
    color: white;
    font-weight: 700;
}
</style>