<template>
  <div class="home">
    <Searchbar @onSearch="handleOnSearch" />

    <!-- How it works section -->
    <section class="mb-5">
      <div class="row">
        <div class="col-12 col-md-7 mb-3">
          <h1 class="fw-bold mb-4">Rent a car your way</h1>
          <h3 class="fw-normal">
            Flexible <span class="fw-bold">pickup</span>. Or get them
            <span class="fw-bold">delivered</span>.
          </h3>
          <h3 class="mb-4 fw-normal">Travel more. Worry less.</h3>
          <button type="button" class="btn btn-primary-theme fw-bold">
            How it works
          </button>
        </div>
        <div class="col-12 col-md-5">
          <img
            src="../assets/hero-image.jpg"
            class="img-fluid rounded"
            alt="hero image"
          />
        </div>
      </div>
    </section>

    <!-- Deals section -->
    <section class="mb-5">
      <h3 class="fw-bold">Check out our deals today</h3>
      <div class="row gx-5">
        <div class="col-12 col-md-6 col-lg-3 mb-3">
          <div class="card text-decoration-none" href="#">
            <img
              src="../assets/deal-image-1.jpg"
              class="card-img-top"
              alt="deal image 1"
            />
            <div class="card-body">
              <h5 class="card-title fw-bold">Subaru Outback</h5>
              <p class="card-text fs-2 text-accent fw-bold">
                $20/day
                <span
                  class="fs-6 fw-normal text-muted text-decoration-line-through"
                  >$40/day</span
                >
              </p>
            </div>
          </div>
        </div>
        <div class="col-12 col-md-6 col-lg-3 mb-3">
          <div class="card text-decoration-none" href="#">
            <img
              src="../assets/car-1.jpg"
              class="card-img-top"
              alt="deal image 1"
            />
            <div class="card-body">
              <h5 class="card-title fw-bold">Toyota TRD</h5>
              <p class="card-text fs-2 text-accent fw-bold">
                $30/day
                <span
                  class="fs-6 fw-normal text-muted text-decoration-line-through"
                  >$40/day</span
                >
              </p>
            </div>
          </div>
        </div>
        <div class="col-12 col-md-6 col-lg-3 mb-3">
          <div class="card text-decoration-none" href="#">
            <img
              src="../assets/car-2.jpg"
              class="card-img-top"
              alt="deal image 1"
            />
            <div class="card-body">
              <h5 class="card-title fw-bold">Jeep Compass</h5>
              <p class="card-text fs-2 text-accent fw-bold">
                $64/day
                <span
                  class="fs-6 fw-normal text-muted text-decoration-line-through"
                  >$90/day</span
                >
              </p>
            </div>
          </div>
        </div>
        <div class="col-12 col-md-6 col-lg-3 mb-3">
          <div class="card text-decoration-none" href="#">
            <img
              src="../assets/car-3.jpg"
              class="card-img-top"
              alt="deal image 1"
            />
            <div class="card-body">
              <h5 class="card-title fw-bold">Tesla X</h5>
              <p class="card-text fs-2 text-accent fw-bold">
                $72/day
                <span
                  class="fs-6 fw-normal text-muted text-decoration-line-through"
                  >$84/day</span
                >
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Why section -->
    <section class="mb-5">
      <h3 class="fw-bold">Why CarToGo?</h3>
      <div class="row">
        <div class="col-12 col-md-6 col-lg-4 mb-2">
          <div class="d-inline-block icon-container text-center">
            <i class="fas fa-car fa-3x"></i>
          </div>
          <div class="d-inline-block ms-3">
            <p class="fw-bold lh-1 mb-0">Free Cancellation</p>
            <small class="fw-light fs-small text-muted"
              >within the first 48hrs</small
            >
          </div>
        </div>
        <div class="col-12 col-md-6 col-lg-4 mb-2">
          <div class="d-inline-block icon-container text-center">
            <i class="fas fa-award fa-3x"></i>
          </div>
          <div class="d-inline-block ms-3">
            <p class="fw-bold lh-1 mb-0">Our Price Guaranteed</p>
            <small class="fw-light fs-small text-muted"
              >best prices for your budget</small
            >
          </div>
        </div>
        <div class="col-12 col-lg-4 mb-2">
          <div class="d-inline-block icon-container text-center">
            <i class="fas fa-hand-sparkles fa-3x"></i>
          </div>
          <div class="d-inline-block ms-3">
            <p class="fw-bold lh-1 mb-0">Cleaning Protocol</p>
            <small class="fw-light fs-small text-muted"
              >FDA compliant to ensure your safety</small
            >
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Searchbar from "@/components/Searchbar";

export default {
  name: "Home",
  components: {
    Searchbar,
  },
  created() {},
  methods: {
    handleOnSearch(searchQuery) {
      // write to localStorage for search page
      localStorage.setItem("searchQuery", JSON.stringify(searchQuery));
      this.$router.push({ name: "Search" });
    },
  },
};
</script>

<style scoped>
.fs-small {
  font-size: 0.75em;
}

.icon-container {
  width: 60px;
  height: 60px;
}

.card-img-top {
  min-height: 214px;
}
</style>
