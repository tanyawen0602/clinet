<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-primary sticky-top">
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>

    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav mr-auto">
        <li class="nav-item active" v-on:click='setUser'>
          <a class="nav-link text-light" href="#"> 账户设置 <span class="sr-only">(current)</span></a>
        </li>
        <li class="nav-item active" v-on:click='account'>
          <a class="nav-link text-light" href="#"> 账户余额 <span class="sr-only">(current)</span></a>
        </li>
        <li class="nav-item active" v-on:click='transaction'>
          <a class="nav-link text-light" href="#"> 转账交易 <span class="sr-only">(current)</span></a>
        </li>
        <li class="nav-item active" v-on:click='transRecord'>
          <a class="nav-link text-light" href="#"> 账户交易记录 <span class="sr-only">(current)</span></a>
        </li>
      </ul>
      <form class="form-inline my-2 my-lg-0">
        <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
      </form>
    </div>
  </nav>
</template>

<script>
  export default {
    data() {
      return {
        paths: []
      };
    },
    methods: {
      setUser: function () {
        this.$store.commit('BLOCK_SET_TOOLBAR', 'setUser');
      },
      account: function () {
        this.$store.commit('BLOCK_SET_TOOLBAR', 'account');
      },
      transaction: function () {
        this.$store.commit('BLOCK_SET_TOOLBAR', 'transaction');
      },
      transRecord: function () {
        this.$store.commit('BLOCK_SET_TOOLBAR', 'transRecord');
      },
    },
  };
</script>

<style scoped>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

</style>
