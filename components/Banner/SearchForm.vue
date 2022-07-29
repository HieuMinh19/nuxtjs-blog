<template>
  <div class="search-form">
    <div class="form-wrap">
      <form>
        <input
          type="radio"
          id="tours"
          name="search-selector"
          v-model="isSearchTours"
          :value="true"
        /><label class="tours-select" for="tours">Tours</label>
        <input
          type="radio"
          id="hotels"
          name="search-selector"
          :value="false"
          v-model="isSearchTours"
        /><label class="tours-select" for="hotels">Hotels</label>
      </form>
      <div v-if="isSearchTours" class="search-box search-tours active">
        <form>
          <div>
            <input
              type="text"
              class="td-selector"
              autocomplete="off"
              placeholder="e.g. Region, city"
            />
            <button class="tj-button1" type="submit">Search</button>
          </div>
        </form>
      </div>
      <div v-else class="search-hotels active">
        <div class="room-search">
          <div class="hotel-fields">
            <div>
              <div class="destination-selector">
                <input
                  type="text"
                  class="td-selector field-box"
                  autocomplete="off"
                  value=""
                  placeholder="Where would you like to go?"
                />
              </div>
            </div>
            <div class="date-range-selector">
              <HotelDatePicker format="DD/MM/YYYY" class="date-picker">
              </HotelDatePicker>
              <button id="apid" class="choose-dates tj-button1">Search</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import HotelDatePicker from "vue-hotel-datepicker";
import "vue-hotel-datepicker/dist/vueHotelDatepicker.css";
export default {
  components: { HotelDatePicker },

  data() {
    return {
      selectedDate: {
        start: new Date(2018, 10, 9),
        end: new Date(2018, 10, 10),
      },
      isSearchTours: true,
    };
  },
};
</script>

<style lang="scss" scoped>
.active {
  display: block;
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
  margin-bottom: 14px;
}

.search-form {
  font-size: 20px;
  line-height: 28px;
  box-sizing: border-box;
  max-width: 800px;

  .form-wrap {
    form {
      font-weight: bold;
      margin-bottom: 20px;
    }
    input[type="radio"] {
      vertical-align: left;
    }
  }

  form {
    margin-top: 7px;

    div {
      position: relative;
      display: flex;
    }

    input.td-selector {
      font-family: "HK Grotesk";
      font-size: 18px;
      line-height: 26px;
      position: relative;
      box-sizing: border-box;
      margin-right: 10px;
      margin-bottom: 14px;
      padding: 10px 11px;
      color: #3e2600;
      border: 1px solid #bebebe;
      flex-grow: 8;
    }
  }
  .tours-select {
    font-size: 18px;
    line-height: 24px;
    position: relative;
    display: inline-block;
    margin-left: 5px;
    cursor: pointer;
    background-repeat: no-repeat;
    background-position: left center;
    background-size: 16px;

    ::before {
      position: absolute;
      bottom: 0;
      left: 0;
      height: 3px;
      content: "";
      transition: width 0.15s ease-in-out, left 0.15s ease-in-out;
      background-color: #0baee6;
    }
  }

  .hotel-fields {
    display: flex;
    justify-content: flex-start;
    flex-wrap: wrap;

    .destination-selector .field-box {
      width: 32vw;
      font-family: "HK Grotesk";
      font-size: 18px;
      box-sizing: border-box;
      margin-right: 10px;
      margin-bottom: 0;
      padding: 10px 11px;
      cursor: pointer;
      color: #3e2600;
      border: 1px solid #bebebe;
      background-color: white;
      margin-top: 10px;
    }

    .date-range-selector {
      display: flex;
      width: 100%;
      margin-top: 10px;

      .date-picker {
        margin-right: 10px;
      }

      .vhd__datepicker__wrapper {
        height: 80%;
      }
    }
  }
}
</style>