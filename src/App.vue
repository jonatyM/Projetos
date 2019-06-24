<template>
  <div id="app">
    <h1>Tarefas</h1>
    <TaskGrid :tasks="tasks"/>
  </div>
</template>

<script>
import TaskGrid from './components/TaskGrid.vue'

export default {
  components: {TaskGrid},
  name: 'app',
  data(){
    return{
      tasks:[
        {name: 'Compra remedio', pending: false},
        {name: 'Pasear com o cachorro', pending: true}
      ]
    }
  }
}
</script>

<style>
body{
  background: #1F1C2C;  /* fallback for old browsers */
  background: -webkit-linear-gradient(to right, #928DAB, #1F1C2C);  /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to right, #928DAB, #1F1C2C); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */

}
 #app{
   display: flex;
   flex: 1;
   flex-direction: column;
   justify-content: center;
   align-items: center;
   height: 100vh;
 }

 #app h1{
   margin-bottom: 5px;
   font-weight: 300;
   font-size: 5rem;
 }
</style>
