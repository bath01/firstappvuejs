<template>
  <div class="wrapper--input">
    <input
      v-model="user_search_restaurant"
      type="text"
      id=""
      placeholder="Search..."
    />
    <div class="search">
      <div
        v-for="(restaurant, i) in search_restaurant"
        :key="i"
        name=""
        class="container--restaurant--search"
      >
        <div class="wrapper--img">
          <img :src="restaurant.image" alt="" />
        </div>
        <p>{{ restaurant.name }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "BoitedeRech",
};
</script>

<style lang="scss">
.wrapper--input {
      position: relative;
      input {
        background-color: #f6f6f6;
        border: none;
        height: 60px;
        width: 400px;
        outline: none;
        padding-left: 20px;
      }
      .search {
        position: absolute;
        top: 100%;
        width: 100%;
        //height: 400px;
        background: #fff;
        //border: 1px solid red;

        .container--restaurant--search {
          display: flex;
          align-items: center;
          padding: 10px;

          &:hover {
            background: #f6f6f6;
          }

          .wrapper--img {
            height: 60px;
            width: 60px;
            margin-right: 25px;
            border-radius: 50%;
            overflow: hidden;

            img {
              height: 100%;
              width: auto;
            }
          }
        }
      }
    }

</style>
