<template>
  <div class="gift">
    <div class="gift-tier-1"></div>
    <div class="gift-tier-2"></div>
    <div class="gift-top"></div>
    <div class="gift-body"></div>

  </div>
</template>

<script>
export default {
    name:'Gift'
};
</script>

<style>

.gift{
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    z-index: 10;
}

.gift-top{
    width: 100px;
    height: 25px;
    background-color: rgb(36, 164, 53);
}

.gift-body{
    width: 90px;
    height: 60px;
    background-color: rgb(44, 140, 57);
}

.gift-tier-1{
    position: absolute;
    width: 15px;
    height: 85px;
    background-color: red;
}
.gift-tier-2{
    position: absolute;
    top: 40px;
    height: 15px;
    width: 90px;
    background-color: red;  
}

</style>