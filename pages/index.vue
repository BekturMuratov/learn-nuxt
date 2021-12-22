<template>
<div>
  <Nav/>
  <div class="container">
   
<hero/>
<div class="top"></div>
<LargeCardDisplay v-for="cardInfo in largeCardInfo" :key="cardInfo.id" :cardSection="cardInfo"/>
 <SmallCardDisplay 
      v-for="cardInfo in smallCardSections"
      :key="cardInfo.id"
      :cardsSection="cardInfo"
    /> 
  </div>
</div>
</template>

<script>
import { largeCardSections, smallCardSections } from "@/assets/data.js"
export default {
  data(){
    return {
      largeCardInfo: largeCardSections,
      smallCardSections: smallCardSections
    }
  }
}
</script>
<style scoped>
.top{
  margin-top:20rem;
}
</style>
