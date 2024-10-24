<template>
  <main>
  <div class="container">
    <h3>Alış-veriş listi 
    </h3>
    <hr>
      <input type="text" placeholder="Nə alacaqsınız?" v-model="inp" @keydown.enter="onSave">
 
    <ul>
      <li v-for="item in li" key="item">
        <span>{{item}}</span>
      <button class="delete">Sil</button>
      </li>
      <li>
        <span>App2</span>
      <button class="delete">Sil</button>
      </li>
      <li>
        <span>App3</span>
      <button class="delete">Sil</button>
      </li>
      <small>5 ədəd məhsul var</small>
    </ul>
  </div>
</main>
</template>

<script>
import axios from "axios"
export default{
  data(){
    return{
  
    }
  },
methods:{
  onSave(e){
  }
}

}
</script>