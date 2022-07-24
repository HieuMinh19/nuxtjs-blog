<template>
  <article class="standard-padding standard-spacing">
    <link
      href="https://cdn.jsdelivr.net/npm/tailwindcss@2.1.2/dist/tailwind.min.css"
      rel="stylesheet"
    />
    <h1>Search Page</h1>
    <br /><br />
    <form method="get" id="search-form" action="https://www.touristisrael.com/">
      <label for="s" class="assistive-text"></label>
      <input
        type="text"
        class="field"
        name="s"
        id="s"
        placeholder="Search for..."
      />
      <input
        type="submit"
        class="submit"
        name="submit"
        id="searchsubmit"
        value="Find"
      />
    </form>
  </article>
</template>

<script>
export default {
  name: "SearchPage",
};
</script>
<style lang="scss" scoped>
article {
  font-size: 20px;
  line-height: 28px;
  position: relative;

  h1 {
    font-size: 54px;
    line-height: 60px;
    position: relative;
    display: block;
    margin-bottom: 40px;
    padding-bottom: 5px;
    text-align: left;
    color: #3e2600;
  }

  #search-form  {
    input.field {
      font-family: 'HK Grotesk';
      font-size: 24px;
      font-weight: normal;
      display: block;
      box-sizing: border-box;
      width: 100%;
      padding: 10px;
      color: #3e2600;
      border: 2px solid #3e2600;
    }

    input.submit {
      font-family: 'bebas-neue-pro-expanded';
      font-size: 32px;
      font-weight: 600;
      line-height: 36px;
      display: block;
      box-sizing: border-box;
      width: auto;
      margin-top: 30px;
      margin-left: auto;
      padding: 10px;
      cursor: pointer;
      transition: color .15s ease-in-out, background-color .15s ease-in-out;
      text-transform: uppercase;
      color: white;
      border: 2px solid #0baee6;
      background-color: #0baee6;
    }
  }
}
</style>

