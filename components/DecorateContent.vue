<template>
  <div class="decorated-content standard-padding">
    <h4 class="double-dotted">Travel With Passion</h4>
    <blockquote>
      <p class="blockqoute">
        Our pledge is a promise that sets apart our entire team.
      </p>
    </blockquote>
    <p>
      We seek out the most passionate professionals, and find the most
      experiential ways to present Israel, its flavors and cultures. For us it’s
      about more than just ticking the boxes on a bucket list, or getting you a
      great Instagram photo. Whilst our guides have done the same trips many
      times, we know that the days when you travel are your only days here. And
      so just like a theater production, we make sure that it will be best day
      ever!
    </p>
    <p class="font-bold">
      <strong
        >It’s about giving all our guests a great feeling, experience, and
        lifelong memories, it’s about sharing our passion and love for what we
        do!</strong
      >
    </p>
    <p class="action-link">
      <a
        href="https://www.touristisrael.com/travel-with-passion/"
        target="_self"
        ><span>Our Philosophy</span></a
      >
    </p>
  </div>
</template>

<style lang="scss" scoped>
.decorated-content {
  padding: 35px 40px 65px 35px;
  background-color: #71d1fe;
  margin-top: 120px;
  margin-bottom: 120px;
  width: 100% !important;

  h4 {
    font-size: 40px;
    line-height: 50px;
    margin-bottom: 50px;
    display: inline-block;
    border-bottom: 2px dotted;
  }

  .blockqoute {
    font-size: 30px;
    font-weight: bold;
    line-height: 29px;
    margin-bottom: 45px;
  }

  p {
    font-size: 20px;
    font-weight: 400;
    line-height: 26px;
    margin-bottom: 45px;
  }

  .double-dotted::after {
    display: block;
    width: 100%;
    margin-bottom: 5px;
    content: "";
    border-bottom: 2px dotted;
  }

  .font-bold {
    font-weight: bold;
  }

  .action-link {
    text-align: right;
    a {
      font-size: 22px;
      font-weight: bold;
      line-height: 32px;
      text-transform: uppercase;
      text-decoration: underline;
    }
  }
  .action-link::after {
    display: inline-block;
    margin-left: 7px;
    content: "\2192";
    transition: 0.15s transform ease-in-out;
    vertical-align: text-bottom;
  }
}
</style>