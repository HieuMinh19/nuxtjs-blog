<template>
  <div id="banner">
    <div class="travel-style-selector-search">
      <div class="search-header">
        <img
          :src="bannerImg"
          alt="Shutterstock 128685680 Scaled"
          width="2000"
          height="800"
        />
        <div class="search-header-decoration"></div>
        <h4>
          Over 100,000 people visit Israel with us every year. Let us make your
          trip perfect
        </h4>
        <SearchForm />
      </div>
    </div>
  </div>
</template>

<script>
import SearchForm from "../Banner/SearchForm";
export default {
  components: { SearchForm },
  data: function () {
    return {
      bannerImg:
        "https://i0.wp.com/www.touristisrael.com/wp-content/uploads/2021/03/shutterstock_128685680-scaled.jpg?resize=2000%2C800&ssl=1",
    };
  },
};
</script>

<style lang="scss" scoped>
.travel-style-selector-search {
  padding-right: 40px;
  background-color: #feef43;

  .search-header {
    position: relative;
    display: block;
    box-sizing: border-box;
    height: 640px;
    min-height: 540px;
    padding: 15vh 45px 40px 60px;

    > img {
      position: absolute;
      top: 0;
      left: 0;
      display: block;
      height: 640px;
      max-height: none;
      margin-bottom: 0;
      object-fit: cover;
      object-position: bottom;
    }

    .search-header-decoration::before {
      position: absolute;
      bottom: calc(-640px - 1px);
      left: 0;
      width: 0;
      height: 0;
      content: "";
      border-width: 4vh 0 0 30vw;
      border-style: solid;
      border-color: transparent transparent transparent #71d1fe;
    }

    .search-header-decoration::after {
      position: absolute;
      right: -236px;
      bottom: calc(-640px - 1px);
      width: 0;
      height: 0;
      content: "";
      border-width: 0 24px 6.85vh 30vw;
      border-style: solid;
      border-color: transparent transparent #0baee6 transparent;
    }

    .search-header-decoration {
      position: absolute;
      top: -1px;
      left: 0;
      width: 0;
      height: 0;
      padding-left: 30vw;
      border-right: 235px solid transparent;
      border-bottom: calc(640px + 1px) solid #feef43;
    }

    h4 {
      font-size: 35px;
      line-height: 42px;
      position: relative;
      max-width: 28vw;
      margin-bottom: 50px;
      text-align: left;
      color: #3e2600;
      font-family: "bebas-neue-pro-expanded";
      font-weight: 600;
      text-decoration: none;
      text-transform: uppercase;
      word-wrap: break-word;
    }

    div {
      font-size: 20px;
      line-height: 24px;
      position: relative;
      width: 32vw;
      max-width: 600px;
      color: #3e2600;
    }
  }
}
</style>