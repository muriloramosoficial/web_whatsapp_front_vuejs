<script>
export default {
  data(){
    return {
      chats: ['Você: Testando chat 1', 'Você: Testando chat 2', 'Você: Testando chat 3', 'Você: Testando chat 4', 'Você: Testando chat 5', 'Você: Testando chat 6'],
      users: ['Murilo Ramos', '+55 (45) 9139-2793', 'User 1', 'User 2', 'User 3', 'User 4'],
      images: [''],
    }
  }
}
</script>

<template>
  <div class="contentChat">
    <!-- <div v-for="imagem in images" :key="imagem">
        <img :src="imagem"/>
    </div>
    <div>
        <div v-for="user in users" :key="user">
            <h2>{{ user }}</h2>
        </div>
        <div v-for="chat in chats" :key="chat">
            <h4>{{ chat }}</h4>
        </div>
    </div> -->
    <div class="imageCard">
        <img class="image" src="../../assets/images/imgPhoto.PNG" width="70" height="70"/>
    </div>
    <div class="middle">
        <div>
            <h3>Murilo Ramos</h3>
        </div>
        <div>
            <h4>Você: Testando chat</h4>
        </div>
    </div>
  </div>
  <div></div>
</template>

<style scoped>
.contentChat{
    display: flex;
    /* justify-content: space-between; */
    flex-direction: row;
    /* background-color: rgb(255, 255, 255); */
    border-right: 2.5px solid #d7dbe0;
    border-bottom: 2.5px solid #d7dbe0c1;
}
.contentChat:hover{
    cursor: pointer;
    background-color: #f0f2f5;
}
.image{
    border-radius: 30px;
}
.imageCard{
    padding: 13px 15px 8px 13px;
}
.middle{
    display: flex;
    justify-content: center;
    flex-direction: column;
    /* align-items: center; */
    padding: 5px 0 10px 0;
    font-size: 18px;
}
h3{
    font-weight: bold;
}
</style>
