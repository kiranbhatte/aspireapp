<template>
  <div class="mainbody d-flex">
    <div class="sidebar">
      <div class="log-description">
        <img src="../assets/AspireLogo.svg" alt="AspireLogo" />
        <p>Trusted way of banking for 3,000+ SMEs and startups in Singapore</p>
      </div>
      <a href="#home"
        ><img alt="Vue logo" src="../assets/Home.svg" class="px-2" />Home</a
      >
      <a class="active" href="#news"
        ><img alt="Vue logo" src="../assets/Card.svg" class="px-2" />Cards</a
      >
      <a href="#contact"
        ><img
          alt="Vue logo"
          src="../assets/Payments.svg"
          class="px-2"
        />Payments</a
      >
      <a href="#about"
        ><img alt="Vue logo" src="../assets/Credit.svg" class="px-2" />Credit</a
      >
      <a href="#about"
        ><img
          alt="Vue logo"
          src="../assets/Account.svg"
          class="px-2"
        />Settings</a
      >
    </div>

    <div class="content">
      <p>Available balance</p>
      <div class="d-flex justify-content-between">
        <div>
          <div class="bal-text"><span class="ss-btn">ss</span> 3,000</div>
        </div>
        <button class="new-card-btn">
          <img alt="Vue logo" src="../assets/box.svg" /> New card
        </button>
      </div>
      <div class="mt-4">
        <ul class="nav nav-tabs card-option" id="myTab" role="tablist">
          <li class="nav-item" role="presentation">
            <button
              class="nav-link active detail-tab"
              id="home-tab"
              data-bs-toggle="tab"
              data-bs-target="#home"
              type="button"
              role="tab"
              aria-controls="home"
              aria-selected="true"
            >
              My debit cards
            </button>
          </li>
          <li class="nav-item" role="presentation">
            <button
              class="nav-link detail-tab"
              id="profile-tab"
              data-bs-toggle="tab"
              data-bs-target="#profile"
              type="button"
              role="tab"
              aria-controls="profile"
              aria-selected="false"
            >
              All company cards
            </button>
          </li>
        </ul>
        <div class="tab-content" id="myTabContent">
          <div
            class="tab-pane fade show active"
            id="home"
            role="tabpanel"
            aria-labelledby="home-tab"
          >
            <div class="card mt-3 card-details">
              <div class="card-body">
                <div class="row">
                  <div class="col-md-6">
                    <cardSlider />
                  </div>
                  <div class="col-md-6">
                    <div class="accordion" id="accordionExample">
                      <div class="accordion-item acard-item">
                        <h2 class="accordion-header" id="headingOne">
                          <button
                            class="accordion-button card-accordion"
                            type="button"
                            data-bs-toggle="collapse"
                            data-bs-target="#collapseOne"
                            aria-expanded="true"
                            aria-controls="collapseOne"
                          >
                            <img
                              alt="Vue logo"
                              src="../assets/carddetail.svg"
                              class="px-2"
                            />
                            Card details
                          </button>
                        </h2>
                        <div
                          id="collapseOne"
                          class="accordion-collapse collapse"
                          aria-labelledby="headingOne"
                          data-bs-parent="#accordionExample"
                        >
                          <div class="accordion-body">
                            <strong
                              >This is the first item's accordion body.</strong
                            >
                            It is shown by default, until the collapse plugin
                            adds the appropriate classes that we use to style
                            each element. These classes control the overall
                            appearance, as well as the showing and hiding via
                            CSS transitions. You can modify any of this with
                            custom CSS or overriding our default variables. It's
                            also worth noting that just about any HTML can go
                            within the <code>.accordion-body</code>, though the
                            transition does limit overflow.
                          </div>
                        </div>
                      </div>
                      <div class="accordion-item acard-item">
                        <h2 class="accordion-header" id="headingTwo">
                          <button
                            class="accordion-button card-accordion collapsed"
                            type="button"
                            data-bs-toggle="collapse"
                            data-bs-target="#collapseTwo"
                            aria-expanded="false"
                            aria-controls="collapseTwo"
                          >
                            <img
                              alt="Vue logo"
                              src="../assets/recenttrans.svg"
                              class="px-2"
                            />
                            Recent transactions
                          </button>
                        </h2>
                        <div
                          id="collapseTwo"
                          class="accordion-collapse collapse show"
                          aria-labelledby="headingTwo"
                          data-bs-parent="#accordionExample"
                        >
                          <div class="accordion-body">
                            <strong
                              >This is the second item's accordion body.</strong
                            >
                            It is hidden by default, until the collapse plugin
                            adds the appropriate classes that we use to style
                            each element. These classes control the overall
                            appearance, as well as the showing and hiding via
                            CSS transitions. You can modify any of this with
                            custom CSS or overriding our default variables. It's
                            also worth noting that just about any HTML can go
                            within the <code>.accordion-body</code>, though the
                            transition does limit overflow.
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div
            class="tab-pane fade"
            id="profile"
            role="tabpanel"
            aria-labelledby="profile-tab"
          >
            <div class="card mt-3 card-details">
              <div class="card-body">This is All company cards Details.</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import cardSlider from "../components/cardSlider.vue";

export default {
  name: "aspireDashboard",
  components: {
    cardSlider,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
body {
  margin: 0;
  font-family: "Lato", sans-serif;
}

.sidebar {
  margin: 0;
  padding: 0;
  width: 270px;
  background-color: #0c365a;
  height: 100vh;
  overflow: auto;
}

.sidebar a {
  display: block;
  color: #ffffff;
  padding: 26px 16px;
  text-align: left;
  text-decoration: none;
}

.sidebar a.active {
  background-color: transparent;
  color: #01d167;
}

.sidebar a:hover:not(.active) {
  background-color: transparent;
  color: #01d167;
}

div.content {
  padding: 40px;
  flex: 1;
}
.bal-text {
  font-weight: 800;
}
.ss-btn {
  background-color: #01d167;
  padding: 4px 12px;
  border-radius: 4px;
  color: white;
  margin-right: 4px;
  font-weight: 400;
}
.log-description {
  text-align: left;
  padding: 30px 20px;
}
.nav-tabs > .detail-tab .nav-item.show .nav-link,
.nav-tabs .detail-tab.active {
  color: #222222;
  background-color: #fff;
  border-color: transparent;
  border-bottom: 2px solid #23cefd;
  padding-bottom: 4px;
  font-weight: 700;
  opacity: 1;
}
.card-option .nav-item {
  padding-right: 20px;
}
.card-details {
  border: 1px solid #fcfcfc;
  box-shadow: 0px 0px 16px #00000014;
  border-radius: 8px;
}
.nav-link.detail-tab {
  color: #222222;
  opacity: 0.4;
}
.nav-tabs .detail-tab {
  padding: 0;
  padding-left: 0;
}
.nav-tabs .nav-link.detail-tab:hover {
  border-color: transparent;
  isolation: isolate;
}
.nav-tabs {
  border-bottom: none;
}
.log-description p {
  padding: 20px 0 0;
  margin: 0;
  color: #ffffff;
  font-size: 14px;
  opacity: 0.3;
}
.new-card-btn {
  border: none;
  background-color: #325baf;
  color: white;
  padding: 4px 10px;
  border-radius: 4px;
  font-size: 14px;
}
.card-accordion:not(.collapsed) {
  color: #0c365a;
  background-color: #f5f9ff;
  box-shadow: 0 0px 6px #0000000a;
  border: none;
}
.accordion-item.acard-item {
  background-color: #ffffff;
  border: 1px solid #f0f0f0;
  border-radius: 8px;
  margin-bottom: 16px;
}
.acard-item:first-of-type .card-accordion {
  border-top-left-radius: 8px;
  border-top-right-radius: 8px;
}
.acard-item:last-of-type .card-accordion.collapsed {
  border-bottom-right-radius: 8px;
  border-bottom-left-radius: 8px;
}
.card-accordion {
  background-color: #f5f9ff;
  border-radius: 8px;
}
.card-accordion::after {
  background-image: url("../assets/down-arrow.svg");
}
.card-accordion:not(.collapsed)::after {
  background-image: url("../assets/down-arrow.svg");
  transform: rotate(-180deg);
}
@media screen and (max-width: 700px) {
  .sidebar {
    width: 100%;
    height: auto;
    position: relative;
  }
  .sidebar a {
    float: left;
  }
  div.content {
    margin-left: 0;
  }
}

@media screen and (max-width: 400px) {
  .sidebar a {
    text-align: center;
    float: none;
  }
}
</style>
