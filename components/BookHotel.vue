<template>
  <div id="book-hotels">
    <div
      v-for="(tour, index) in tours"
      class="book-hotels narrow-margin standard-spacing"
    >
      <div class="left-pane">
        <h2 class="double-dotted">{{ tour.title }}</h2>
        <p>{{ tour.description }}</p>
        <ul>
          <li v-for="url in tour.urls">
            <a :href="url.url" target="_self">{{ url.name }}</a>
          </li>
        </ul>
        <a
          class="tj-button1"
          href="https://www.touristisrael.com/tours/"
          target="_self"
          >Tourist Israel Tours</a
        >
      </div>
      <div class="decoration">
        <img :src="tour.banner_src" width="1024" height="501" />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      tours: [
        {
          title: "TOURIST ISRAEL TOURS",
          description:
            "Over 300 Israel tours, designed by our team of experts, offering a unique way to explore and experience Israel.",
          banner_src:
            "https://i0.wp.com/www.touristisrael.com/wp-content/uploads/2021/04/Sea-.jpg?w=1200&ssl=1",
          urls: [
            {
              name: "Tours to Masada & Dead Sea",
              url: "https://www.touristisrael.com/type/classic-highlights-of-israel-tour-packages/",
            },
            {
              name: "Tours to Jerusalem",
              url: "https://www.touristisrael.com/type/classic-highlights-of-israel-tour-packages/",
            },
            {
              name: "Tours to Petra & Jordan",
              url: "https://www.touristisrael.com/type/classic-highlights-of-israel-tour-packages/",
            },
            {
              name: "Tours to the Galilee",
              url: "https://www.touristisrael.com/type/classic-highlights-of-israel-tour-packages/",
            },
          ],
        },
        {
          title: "ISRAEL PACKAGE TOURS",
          description:
            "Our Israel Package Tours are designed around for a range of travel styles, themes, lengths, and languages, so we aim to have something for everyone.",
          banner_src:
            "https://i0.wp.com/www.touristisrael.com/wp-content/uploads/2021/04/Israel-Packages-Tour.jpg?w=2048&ssl=1",
          urls: [
            {
              name: "Classic Highlights of Israel Tour Packages",
              url: "https://www.touristisrael.com/type/classic-highlights-of-israel-tour-packages/",
            },
            {
              name: "Christian Holy Land Tour Packages",
              url: "https://www.touristisrael.com/type/classic-highlights-of-israel-tour-packages/",
            },
            {
              name: "Jewish Israel Tour Packages",
              url: "https://www.touristisrael.com/type/classic-highlights-of-israel-tour-packages/",
            },
          ],
        },
        {
          title: "HOTELS",
          description:
            "Book your Israel Hotels with Tourist Israel and take advantage of our selection of the country's best places to stay, many with special benefits.",
          banner_src:
            "https://i0.wp.com/www.touristisrael.com/wp-content/uploads/2021/03/IsraelHotels.jpg?w=1200&ssl=1",
          urls: [
            {
              name: "Tel Aviv Hotels",
              url: "https://www.touristisrael.com/type/classic-highlights-of-israel-tour-packages/",
            },
            {
              name: "Jerusalem Hotels",
              url: "https://www.touristisrael.com/type/classic-highlights-of-israel-tour-packages/",
            },
            {
              name: "Eilat Hotels",
              url: "https://www.touristisrael.com/type/classic-highlights-of-israel-tour-packages/",
            },
            {
              name: "Northern Israel Hotels",
              url: "https://www.touristisrael.com/type/classic-highlights-of-israel-tour-packages/",
            },
          ],
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.narrow-margin {
  width: calc(100% - 80px);
  margin-right: 40px;
  margin-left: 40px;
}
.book-hotels:nth-of-type(odd) {
  flex-direction: row-reverse;
}
.book-hotels {
  display: flex;
  flex-direction: row;

  h2 {
    font-size: 40px;
    line-height: 54px;
    display: inline-block;
    margin-bottom: 30px;
    color: #0baee6;
    border-bottom: 2px dotted;
  }

  .double-dotted::after {
    display: block;
    width: 100%;
    margin-bottom: 5px;
    content: "";
    border-bottom: 2px dotted;
  }

  .left-pane {
    width: 100%;
    padding: 50px 60px;
    border: 1px solid #dad9c5;
    background-color: white;

    p {
      font-size: 18px;
      line-height: 26px;
      display: block;
      margin-bottom: 27px;
      color: #3e2600;
    }

    ul {
      margin-bottom: 45px;
      list-style: none;
      font-weight: normal;
      line-height: 20px;
      color: #3e2600;

      li {
        font-size: 18px;
        line-height: 26px;
        display: block;
        margin-bottom: 10px;
        padding-left: 0;
        position: relative;

        a {
          text-decoration: underline;
        }
      }
    }
  }
  .tj-button1 {
    font-family: "bebas-neue-pro-expanded";
    font-size: 20px;
    font-weight: 600;
    line-height: 24px;
    display: inline-block;
    padding: 13px 10px 11px 13px;
    cursor: pointer;
    transition: background-color 0.15s ease-in-out;
    text-align: center;
    text-transform: uppercase;
    color: white;
    border: none;
    background-color: #0baee6;
  }
  .tj-button1:not(.no-arrow)::after {
    display: inline-block;
    margin-left: 5px;
    padding-right: 5px;
    content: " \0203a";
    transition: margin 0.15s ease-in-out, padding 0.15s ease-in-out;
  }

  .decoration {
    z-index: 1;
    display: flex;
    overflow: hidden;
    width: 100%;
    min-height: 50vh;
    max-height: 100%;
    flex: 1 0 50%;
    align-items: center;
    justify-content: center;

    img {
      width: 100%;
      height: 100%;
    }
  }
}
.standard-spacing {
  margin-top: 120px;
  margin-bottom: 120px;
}
</style>