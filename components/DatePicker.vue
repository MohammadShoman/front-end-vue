<template>
  <div class="Date-of-birth">
      <div class="birthday ">
                  <p>Birthday</p>
                  <img
                    class="icon"
                    src="https://img.icons8.com/emoji/48/000000/white-question-mark-emoji.png"
                  />
                </div>
                <div  class="date-picker">
    <form class="form">
      <select name="month" id="month" class="input-date">
        <option :key="index" v-for="(item, index) in months" :value="item">
          {{ item }}
        </option>
      </select>
    </form>
    <form class="form">
      <select name="day" id="day" class="input-date">
        <option :key="index" v-for="(item, index) in days" :value="item">
          {{ item }}
        </option>
      </select>
      
    </form>
    <form class="form">
      <select name="year" id="year" class="input-date">
        <option :key="index" v-for="(item, index) in years" :value="item">
          {{ item }}
        </option>
      </select>
    </form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
       items: ['Foo', 'Bar', 'Fizz', 'Buzz'],
      years: [
        2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012, 2011,
        2010, 2009, 2008, 2007, 2006, 2005, 2004, 2003, 2002, 2001, 2000, 1999,
        1998, 1997, 1996, 1995, 1994, 1993, 1992, 1991, 1990, 1989, 1988, 1987,
        1986, 1985, 1984, 1983, 1982, 1981, 1980, 1979, 1978, 1977, 1976, 1975,
        1975, 1974, 1973, 1972, 1971, 1970, 1969, 1968, 1967, 1966, 1965, 1964,
        1963, 1962, 1961, 1960,
      ],
      days: [
        1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20,
        21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31,
      ],
      months: [
        "jan",
        "Feb",
        "Mar",
        "Apr",
        "May",
        "Jan",
        "Jul",
        "Aug",
        "Sep",
        "Oct",
        "Nov",
        "Dec",
      ],
    };
  },
};
</script>

<style>
.input-date {
  width: 126px;
  padding-left: 10px;
  border-radius: 5px;
  border: 2px solid #dddfe2;
  height: 35px;
}
.input-date:focus {
  outline: none !important;
}
.date-picker {
  display: flex;
  width: 90%;
  justify-content: center;
  align-items: center;
  margin-left: 14px;
}
.form {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-left: 17px;
  margin-top: 20px;
}

.Date-of-birth{
    display: flex;
    flex-direction:column;
}
.icon {
  background-color: #606770;
  height: 15px;
  width: 15px;
  border-radius: 50%;
  margin-left: -40px;
  margin-top: 23px;
}
.birthday {
  display: flex;
  margin-left: 16px;
  margin-bottom: -30px;
  color:#606770;
  font-weight: 300;
  font-size:0.8rem
}
</style>
