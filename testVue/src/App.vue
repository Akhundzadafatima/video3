<template>
  <main>
  <div class="container">
    <h3>Alış-veriş listi 
    </h3>
    <hr>
      <input type="text" placeholder="Nə alacaqsınız?" @keydown.enter="onSave">
 
    <ul>
      <li>
        <span>App1</span>
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
    const saveObject={
      title:e.target.value,
      createdt_at:new Date(),
      complated: false
    };
axios.post("http://localhost:3000/items", saveObject).then(save_response=>{
  console.log(save_response);
  
})
}
}
}
</script>