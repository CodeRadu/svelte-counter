<script lang="ts">
  let count=0
  function add(){
    count+=1
    localStorage.setItem('countr-count', count.toString())
  }
  function getCount(){
    count=+localStorage.getItem('countr-count')
  }
  function reset(){
    count=0
    localStorage.removeItem('countr-count')
  }
  getCount()
</script>

<main>
  <button class="waves-effect waves-light btn" on:click={add}>Clicked {count} times</button>
  <br>
  <button class="waves-effect waves-light btn" on:click={reset}>Reset count</button>
</main>