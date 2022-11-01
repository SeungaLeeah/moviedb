<template>
  <div>
    <img class="mainLogo" src="../assets/imgs/mainlogo.png" alt="mainlogo"/>
    <div class="text-container">
        <ul>
            <li>영화</li>
            <li>TV프로그램</li>
            <li>인물</li>
            <li>More</li>
        </ul>
    </div>
  </div>
</template>

<script>
export default {
    // eslint-disable-next-line vue/multi-word-component-names, vue/no-reserved-component-names
    name: 'Header',
}
</script>

<style scoped>
  .mainLogo{
    height: 100px;
    width: 100px;
  }
</style>
