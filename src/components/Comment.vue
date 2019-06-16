<template>
<div class="container">
  <div v-for="index in 9" :key="index" :class="`grid-item-${index}`">
    <input type="text" placeholder="請輸入名字"><br>
    <textarea placeholder="寫點什麼吧！" rows="4" cols="10" maxlength="100"></textarea>
  </div>
</div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
.container{
    margin:5vw;
    display: grid;
    grid-template-columns: repeat(3,1fr);
    grid-template-rows: repeat(3,25vw);
    grid-column-gap: 5rem;
    grid-row-gap: 8rem;
}

.container div{
    background-color:#fdff99;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

input,textarea{
    font-family: '微軟正黑體';
    font-size: 1rem;
    text-align: center;
    margin: 2vw;
    background: none;
    border: none;
    line-height: 30px;
    overflow:hidden;
    resize: none;
}

/* -------------------rwd------------------- */

@media screen and (max-width: 400px){
.container{
    margin:10vw;
    display: grid;
    grid-template-columns: repeat(1,1fr);
    grid-template-rows: repeat(9,70vw);
    grid-column-gap: 5rem;
    grid-row-gap: 2rem;
}

.container div{
    background-color:#fdff99;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

input,textarea{
    font-family: '微軟正黑體';
    font-size: 1rem;
    text-align: center;
    margin: 2vw;
    background: none;
    border: none;
    line-height: 30px;
    overflow:hidden;
    resize: none;
}

}
</style>
