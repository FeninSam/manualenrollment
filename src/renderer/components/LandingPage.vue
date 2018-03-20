<template>
  <div id="" style="border-radius:5px;height:500px;background-color:white">
   <h2 style="text-align:center;background-color:#008487;color:white;border-radius:5px 5px 0px 0px;height:10%">Onesource Enrollment Status</h2>
    <div>
    
    </div>
  </div>
</template>

<script>
  
import axios from "axios"
  export default {
    name: 'landing-page',
    methods: {
      open (link) {
        this.$electron.shell.openExternal(link)
      }
    },
    data:function(){
      return {
      sampleData:"Nice"
      }
    },
    mounted:function(){
      axios('https://jsonplaceholder.typicode.com/posts/1').then(json => {
    this.sampleData=json.data.title;
  })
    }
  }
</script>

<style>
input[type="submit"],
input[type="reset"],
input[type="button"],
input[type="text"],
button,
textarea {
	-webkit-app-region: no-drag;
}
  @import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');

  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body { font-family: 'Source Sans Pro', sans-serif;
  -ms-overflow-style: scrollbar;
    -webkit-app-region:drag;
   }

  #wrapper {
    background:
      radial-gradient(
        ellipse at top left,
        rgba(255, 255, 255, 1) 40%,
        rgba(229, 229, 229, .9) 100%
      );
    height: 100%;
    padding: 60px 80px;
    width: 100%;
  }

  #logo {
    height: auto;
    margin-bottom: 20px;
    width: 300px;
  }

  main {
    display: flex;
    justify-content: space-between;
  }

  main > div { flex-basis: 50%; }

  .left-side {
    display: flex;
    flex-direction: column;
  }

  .welcome {
    color: #555;
    font-size: 23px;
    margin-bottom: 10px;
  }

  .title {
    color: #2c3e50;
    font-size: 20px;
    font-weight: bold;
    margin-bottom: 6px;
  }

  .title.alt {
    font-size: 18px;
    margin-bottom: 10px;
  }

  .doc p {
    color: black;
    margin-bottom: 10px;
  }

  .doc button {
    font-size: .8em;
    cursor: pointer;
    outline: none;
    padding: 0.75em 2em;
    border-radius: 2em;
    display: inline-block;
    color: #fff;
    background-color: #4fc08d;
    transition: all 0.15s ease;
    box-sizing: border-box;
    border: 1px solid #4fc08d;
  }

  .doc button.alt {
    color: #42b983;
    background-color: transparent;
  }
</style>
