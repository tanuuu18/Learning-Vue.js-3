<template>
  
  <h2 v-bind:id="headingId">Heading</h2>
  <button v-bind:disabled="isDisabled">Bind</button>
  <h2 class="underline">Underlined text</h2>
  <h2 class="underline"  v-bind:class="status">Status</h2>
  <h2 v-bind:class="isPromoted && 'promoted'">Promoted Movie</h2>
  <!-- Conditional Binding of class -->
  <h2 v-bind:class="isSoldout ? 'sold-out':'new'">Soldout ? movie</h2>
  <!-- Array binding of class -->
  <h2 v-bind:class="['new','promoted']">Newly promoted movie</h2>
  <h2 v-bind:class="[isPromoted && 'promoted',isSoldout ? 'sold-out':'new']">Array conditional movie</h2>
  <!-- Object binding of class -->
  <h2 v-bind:class="{
    promoted: isPromoted,
    new: !isSoldout,
    'sold-out':isSoldout
  }">Object conditional movie</h2>

  <!-- Object syntax -->
 <!-- font-size is not a single word so, append it with ''.
 instead of this we can use camel-case i.e. fontSize -->
  <h2 v-bind:style="{
    color:highlightColor,
    fontSize:headerSize+'px',
    padding:'20px'
  }">Inline Style</h2>

  <h2 v-bind:style="headerStyleObject">Style Object</h2>
  <!-- Array syntax -->
  <!-- override the previous style object if same property changes -->
  <div v-bind:style="[baseStyleObject,successStyleObject]">Success Style</div>
  <div v-bind:style="[baseStyleObject,dangerStyleObject]">Danger Style</div>
  
</template>

<script>


export default {
  name: 'App',
  data(){
    return {
      headingId:"heading",
      isDisabled:true,
      status:"success",
      isPromoted:true,
      isSoldout:true,
      highlightColor:'orange',
      headerSize:50,
      headerStyleObject:{
        color:"orange",
         fontSize:'50px',
        padding:'20px'
      },
      baseStyleObject:{
         fontSize:"50px",
        padding:"10px",
      },
      successStyleObject:{
        color:"green",
        backgroundColor:"lightgreen",
        border:"1px solid green",
        padding:"20px"
      },
     dangerStyleObject:{
      color:"darked",
      backgroundColor:"red",
      border:"1px solid darked",
     },
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
  .underline{
  text-decoration: underline;
}
  
.promoted{
  font-style: italic;
}
.new{
  color: olivedrab;
}

.sold-out{
  color: red;
}
</style>
