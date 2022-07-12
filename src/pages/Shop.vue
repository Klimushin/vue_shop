<template>
  <div class="wrapper-content wrapper-content--fixed">
    <section>
      <div class="container">
        <h1>Shop page</h1>
        <div class="item_wrapper">
           <ShopItem
              v-for="item in shopList" :key="item.id"
              :product="item"
           />
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import ShopItem from "@/components/ShopItem";
export default {
  name: "Shop",
  components: {ShopItem},

  comments: {
    ShopItem
  },
  data () {
    return {
      shopList: null
    }
  },
  created() {
    this.shopList = this.$store.getters.getShopList
    console.log(this.shopList)
  }
}
</script>

<style scoped>

</style>