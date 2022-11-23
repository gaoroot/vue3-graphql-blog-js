<template>
    <div class="about">
        <h1>{{ msg }}</h1>
        <p>Счётчик нажатий: <strong>{{ count }}</strong></p>
        <button @click="count++">Счётчик нажатий</button>
    </div>

    <table class="table">
        <thead>
            <tr>
                <th scope="col">#</th>
                <th scope="col">First</th>
                <th scope="col">Last</th>
                <th scope="col">Handle</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <th scope="row">1</th>
                <td>Mark</td>
                <td>Otto</td>
                <td>{{ count }}</td>
            </tr>
        </tbody>
    </table>

</template>

<script>
export default {
  name: 'AboutComponent',
  data() {
    return {
      count: 0,
    }
  },
  created(){
        document.title = "Страница | About" //title
    },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
button {
    font-weight: bold;
    background-color: #42b983;  
    border: none;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    border-radius: 10px;
    border: 2px solid #2c3e50;
}
button:hover {
    box-shadow: 0 12px 16px 0 rgba(0,0,0,0.24), 0 17px 50px 0 rgba(0,0,0,0.19);
}
button:active {
  background-color: #42b983;
  box-shadow: 0 12px 16px 0 rgba(0,0,0,0.24), 0 17px 50px 0 rgba(0,0,0,0.19);
  transform: translateY(4px);
}
</style>
