<template>
  <div>
    <pre>
      {{ JSON.stringify(formValues, null, 2) }}
    </pre>
  </div>
  <!-- Job search form -->
  
 <!-- Prevent modifier : equivalent to e.preventDefault() -->
  <!-- stop the refreshing when you click on submit button -->
  <form @submit.prevent="submitForm">
    <!-- Step 2: Add HTML tag -->
    <!-- Step 3:bind the data properties using v-model directives -->
    <div>
      <label for="name">Name</label>
      <!-- Trim modifier: which eliminates ehite space -->
      <!-- Lazy modifier : modifies the data only when tha change event occurs -->
      <input type="text" id="name" v-model.trim.lazy="formValues.name" />
    </div>
    <div>
      <label for="profile">Profile Summary</label>
      <textarea id="profile" v-model="formValues.profileSummary" />
    </div>

    <!-- Single select dropdown -->
    <div>
      <label for="country">Country</label>
      <select id="country" v-model="formValues.country">
        <option value="">Select a Country</option>
        <option value="india">India</option>
        <option value="vietnam">Vietnam</option>
        <option value="singapore">Singapore</option>
      </select>
    </div>

    <!-- Multi-select dropdown -->
    <div>
      <label for="job-location">Job Location</label>

      <select id="job-location" multiple v-model="formValues.jobLocation">
        <option value="india">India</option>
        <option value="vietnam">Vietnam</option>
        <option value="singapore">Singapore</option>
      </select>
    </div>
     <!-- Single check box -->
    <div>
      <!-- if you want true/false -->
      <!-- <input
        type="checkbox"
        id="remoteWork"
        v-model="formValues.remoteWork"
      /> -->
      <!-- if you wany yes / no -->
      <input
        type="checkbox"
        id="remoteWork"
        v-model="formValues.remoteWork"
        true-value="yes"
        false-value="no"
      />
      <label for="remoteWork">Open to remote work ?</label>
    </div>

    <!-- Multiple Checkboxes -->
    <div>
      <label>Skill set</label>
      <input
        type="checkbox"
        id="html"
        value="html"
        v-model="formValues.skillSet"
      />
      <label for="html">HTML</label>
      <input
        type="checkbox"
        id="css"
        value="css"
        v-model="formValues.skillSet"
      />
      <label for="css">CSS</label>
      <input
        type="checkbox"
        id="javascript"
        value="javascript"
        v-model="formValues.skillSet"
      />
      <label for="javascript">JavaScript</label>
    </div>

    <!-- Radio group -->
    <div>
      <label>Years of Experience</label>
      <input
        type="radio"
        id="0-2"
        value="0-2"
        v-model="formValues.yearsOfExperience"
      />
      <label for="0-2">0-2</label>
      <input
        type="radio"
        id="3-5"
        value="3-5"
        v-model="formValues.yearsOfExperience"
      />
      <label for="3-5">3-5</label>
      <input
        type="radio"
        id="6-10"
        value="6-10"
        v-model="formValues.yearsOfExperience"
      />
      <label for="6-10">6-10</label>
      <input
        type="radio"
        id="10+"
        value="10+"
        v-model="formValues.yearsOfExperience"
      />
      <label for="10+">10+</label>
    </div>
         <!-- 
Key Modifier: when you want a method to be called when a particular key is
pressed -->

    <!-- Want to submit form when user hit enter on age -->
    <div>
      <label for="age">Age</label>
      <!-- Numbered modifier -->
      <!-- Key modifier -->
      <input
        @keyup.enter="submitForm"
        type="number"
        id="age"
        v-model.number="formValues.age"
      />
   </div>
    <!-- Submit button -->
    <!-- Comment for key modifier -->
    <!-- <div>
      <button>Submit</button>
    </div> -->
  </form>
</template>

<script>


export default {
  name: 'App',
  data(){
    return {
       // Step: 1  create data properties
      formValues: {
        name: "",

        profileSummary: "",

        //Single select dropdown
        country: "",

        // multi-select dropdown
        jobLocation: [],

        //Single checkbox
        //if you want true/false
        //remoteWork: "false",

        //if you wany yes / no
        remoteWork: "no",

        //Multiple checkbox
        skillSet: [],

        //Radio group
        yearsOfExperience: "",

        //for number modifier
        age: null,
      
      },
    };
  },
   methods: {
     submitForm() {
       //comment it because added prevent modifier on submit method
      // event.preventDefault();
      console.log("Form values: ", this.formValues);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
label {
  font-weight: bold;
  display: flex;
  margin-bottom: 5px;
}

input + label {
  font-weight: bold;
  display: inline-flex;
  margin-right: 20px;
}

input[type="text"],
textarea,
select {
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.42857143;
  color: #555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 4px;
}
</style>
