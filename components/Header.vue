<template>
  <div id="header">
    <div class="top-bar">
      <ul>
        <li>
          <a href="#">About</a>
        </li>
        <li><a href="#">contact</a></li>
        <li><a href="#">login</a></li>
        <li><a href="#">Sign Up</a></li>
      </ul>
    </div>
    <header class="header" role="banner">
      <div class="left-pane">
        <a
          class="ti-logo"
          href="https://www.touristisrael.com"
          style="background-color: rgb(249, 134, 77)"
          ><img
            src="https://www.touristisrael.com/wp-content/themes/tourist-israel/images/logo-ti.svg"
            alt="Tourist Israel Logo"
            loading="eager"
          />
          <p>Tours</p></a
        >
      </div>

      <nav>
        <div class="nav-menu">
          <ul>
            <li>TOURS & THINKS TO DO</li>
            <li>PACKAGES</li>
            <li>HOTELS & STAYS</li>
            <li>PLACES TO VISIT</li>
            <li>SEARCH</li>
          </ul>
        </div>
      </nav>
    </header>
  </div>
</template>

<style lang="scss" scoped>
#header {
  font-family: "bebas-neue-pro-expanded";

  .top-bar {
    display: flex;
    justify-content: flex-end;
    padding: 0 7.4%;
    background-color: #fdfcec;

    li {
      display: inline;
      list-style: none;
      border-right: 1px solid #938a82;
      margin-top: 1px;
      vertical-align: middle;
      padding: 0 12px 0 8px;

      a {
        font-size: 14px;
        line-height: 16px;
        color: #151209;
        text-transform: capitalize;
        text-decoration: none;
      }
    }
  }

  header {
    position: relative;
    z-index: 140000;
    display: flex;
    padding: 0 7.4%;
    background-color: #feef43;
    justify-content: space-between;

    .ti-logo {
      position: absolute;
      z-index: 1000000;
      top: -40px;
      display: block;
      width: 200px;
      transition: background-color 0.1s ease-in-out;
      background-color: #f5854c;

      p {
        font-size: 24px;
        font-weight: 600;
        line-height: 36px;
        position: absolute;
        bottom: 0;
        padding: 10px 18px;
        text-transform: uppercase;
        color: #feef43;
        margin: unset;
      }
    }
    .lef-banner {
      display: flex;
      min-height: 90px;
    }

    nav {
      .nav-menu {
        ul li {
          min-height: 90px;
          font-size: 24px;
          font-weight: 600;
          line-height: 40px;
          color: inherit;
          display: inline-flex;
          margin: 0 0 0 30px;
          list-style: none;
          transition: color 0.15s ease-in-out;
          text-transform: uppercase;
          align-items: center;
        }
      }
    }
  }

  @media only screen and (max-width: 1400px) {
    nav {
      padding: 0 40px;
    }
  }
}
</style>