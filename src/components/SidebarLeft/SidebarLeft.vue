<script>
import ChatList from './ChatList.vue';

export default {
    data() {
        return {
            isFocused: false
        };
    },
    watch: {
      isFocused(newValue) {
        if (newValue) {
          this.$nextTick(() => {
            this.$refs.input.focus();
          });
        }
      }
    },
    components: { ChatList }
};
</script>

<template>
  <div class="content">
    <div class="header">
      <div class="imagePhoto">
        <img class="photo" src="../../assets/images/imgPhoto.PNG" width="55" height="55"/>
      </div>
      <div class="iconsRight">
        <div class="iconRight"><svg viewBox="0 0 24 24" height="32" width="32" preserveAspectRatio="xMidYMid meet" class="" version="1.1" id="df9d3429-f0ef-48b5-b5eb-f9d27b2deba6" x="0px" y="0px" enable-background="new 0 0 24 24" xml:space="preserve"><path fill="currentColor" d="M12.072,1.761c-3.941-0.104-7.579,2.105-9.303,5.65c-0.236,0.486-0.034,1.07,0.452,1.305 c0.484,0.235,1.067,0.034,1.304-0.45c1.39-2.857,4.321-4.637,7.496-4.553c0.539,0.02,0.992-0.4,1.013-0.939s-0.4-0.992-0.939-1.013 C12.087,1.762,12.079,1.762,12.072,1.761z M1.926,13.64c0.718,3.876,3.635,6.975,7.461,7.925c0.523,0.13,1.053-0.189,1.183-0.712 c0.13-0.523-0.189-1.053-0.712-1.183c-3.083-0.765-5.434-3.262-6.012-6.386c-0.098-0.53-0.608-0.88-1.138-0.782 C2.178,12.6,1.828,13.11,1.926,13.64z M15.655,21.094c3.642-1.508,6.067-5.006,6.201-8.946c0.022-0.539-0.396-0.994-0.935-1.016 c-0.539-0.022-0.994,0.396-1.016,0.935c0,0.005,0,0.009,0,0.014c-0.107,3.175-2.061,5.994-4.997,7.209 c-0.501,0.201-0.743,0.769-0.543,1.27c0.201,0.501,0.769,0.743,1.27,0.543C15.642,21.1,15.648,21.097,15.655,21.094z"></path><path fill="#009588" d="M19,1.5c1.657,0,3,1.343,3,3s-1.343,3-3,3s-3-1.343-3-3S17.343,1.5,19,1.5z"></path></svg></div>
        <div class="iconRight"><svg viewBox="0 0 24 24" height="32" width="32" preserveAspectRatio="xMidYMid meet" class="" version="1.1" x="0px" y="0px" enable-background="new 0 0 24 24" xml:space="preserve"><path fill="currentColor" enable-background="new    " d="M19.005,3.175H4.674C3.642,3.175,3,3.789,3,4.821V21.02 l3.544-3.514h12.461c1.033,0,2.064-1.06,2.064-2.093V4.821C21.068,3.789,20.037,3.175,19.005,3.175z M14.016,13.044H7.041V11.1 h6.975V13.044z M17.016,9.044H7.041V7.1h9.975V9.044z"></path></svg></div>
        <div class="iconRightMenu"><svg viewBox="0 0 24 24" height="32" width="32" preserveAspectRatio="xMidYMid meet" class="" version="1.1" x="0px" y="0px" enable-background="new 0 0 24 24" xml:space="preserve"><path fill="currentColor" d="M12,7c1.104,0,2-0.896,2-2c0-1.105-0.895-2-2-2c-1.104,0-2,0.894-2,2 C10,6.105,10.895,7,12,7z M12,9c-1.104,0-2,0.894-2,2c0,1.104,0.895,2,2,2c1.104,0,2-0.896,2-2C13.999,9.895,13.104,9,12,9z M12,15 c-1.104,0-2,0.894-2,2c0,1.104,0.895,2,2,2c1.104,0,2-0.896,2-2C13.999,15.894,13.104,15,12,15z"></path></svg></div>
      </div>
    </div>
    <div class="search">
      <div class="inputManipulate">
        <div v-if="isFocused">
          <svg viewBox="0 0 24 24" height="27" width="27" preserveAspectRatio="xMidYMid meet" class="iconSearchReturn" version="1.1" x="0px" y="0px" enable-background="new 0 0 24 24" xml:space="preserve"><path fill="#00a884" d="M12,4l1.4,1.4L7.8,11H20v2H7.8l5.6,5.6L12,20l-8-8L12,4z"></path></svg>
        </div>
        <div v-else @click="isFocused = true">
          <svg viewBox="0 0 24 24" height="30" width="30" preserveAspectRatio="xMidYMid meet" class="iconSearch" version="1.1" x="0px" y="0px" enable-background="new 0 0 24 24" xml:space="preserve"><path fill="currentColor" d="M15.009,13.805h-0.636l-0.22-0.219c0.781-0.911,1.256-2.092,1.256-3.386 c0-2.876-2.332-5.207-5.207-5.207c-2.876,0-5.208,2.331-5.208,5.207s2.331,5.208,5.208,5.208c1.293,0,2.474-0.474,3.385-1.255 l0.221,0.22v0.635l4.004,3.999l1.194-1.195L15.009,13.805z M10.201,13.805c-1.991,0-3.605-1.614-3.605-3.605 s1.614-3.605,3.605-3.605s3.605,1.614,3.605,3.605S12.192,13.805,10.201,13.805z"></path></svg>
        </div>
        <input class="inputSearch" type="text" placeholder="Pesquisar ou começar uma nova conversa" @focus="isFocused = true" @blur="isFocused = false" v-if="isFocused" ref="input">
        <input class="inputSearch" type="text" placeholder="Pesquisar ou começar uma nova conversa" @focus="isFocused = true" @blur="isFocused = false" v-else>
      </div>
      <div class="iconFilter">
        <svg viewBox="0 0 24 24" height="27" width="26" preserveAspectRatio="xMidYMid meet" class="" version="1.1" x="0px" y="0px" enable-background="new 0 0 24 24" xml:space="preserve"><path fill="currentColor" d="M10,18.1h4v-2h-4V18.1z M3,6.1v2h18v-2H3z M6,13.1h12v-2H6V13.1z"></path></svg>
      </div>
    </div>
    <div class="chatlist">
      <ChatList/>
    </div>
  </div>
</template>

<style>
.content{
  display: flex;
  justify-content:center;
  flex-direction: column;
}
.header{
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 25px 16.5px 25px;
  width: 578px;
  height: 80px;
  background-color: #f0f2f5;
  border-right: 2.5px solid #d7dbe0;
}
.photo{
  margin-top: 3px;
  border-radius: 30px;
}
.iconsRight{
  display: flex;
  justify-content: center;
  align-items: center;
  padding-top: 6px;
}
.iconRight{
  padding: 17px;
  color: #54656f;
}
.iconRight:hover{
  cursor: pointer;
}
.iconRightMenu{
  padding: 17px 17.5px 17px 17px;
  margin-right: -1px;
  color: #54656f;
}
.iconRightMenu:hover{
  cursor: pointer;
}
.search{
  display: flex;
  justify-content: space-between;
  /* margin: -10px 0 0 0; */
  padding: 10px 0 10px 15px;
  border-right: 2.5px solid #d7dbe0;
  border-bottom: 2.5px solid #d7dbe0c1;
}
.iconSearch{
  margin-right: -40px;
  margin-left: 10px;
  margin-bottom: -22px;
  z-index: 1;
}
.iconSearch:hover{
  cursor: pointer;
}
.iconSearchReturn{
  margin-right: -40px;
  margin-left: 10px;
  margin-bottom: -22px;
  z-index: 1;
}
.iconSearchReturn:hover{
  cursor: pointer;
}
.inputSearch{
  width: 505px;
  background-color: #f0f2f5;
  border: none;
  padding: 16.5px 16.5px 16.5px 60px;
  border-radius: 13px;
  font-size: 18px;
}
.inputSearch:focus{
  box-shadow: none;
  outline: none;
}
.inputManipulate{
  display: flex;
}
.iconFilter{
  color: #8696a0;
  font-weight: bold;
  margin: 12px 17px 0 0;
}
.iconFilter:hover{
  cursor: pointer;
}
</style>
