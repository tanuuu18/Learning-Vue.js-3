# Watchers

Allow you to watch any data or computed property and execute some code in response to changes in the value.

### Example

<ul>
<li>Implement a volume tracker</li>
<li>See the current volume level</li>
<li>Increase or decrease the volume level</li>
</ul>

# Watchers vs Computed Properties

Can I use watchers instead of computed properties?

Yes, Watchers simply provide a more generic way to react to data changes.

However, it is not recommended to mimic a computed property as a watcher.


### fullName as Computed Properties
```
computed:{
    fullName(){
        return `${this.firstName} ${this.lastName}`
    }
}

```

### fullName using Watchers
```
data(){
    return {
        firstName: "",
        lastName: "",
        fullName: ""
    }
},
watch{
    firstName(value){
        this.fullName = value + " " + this.lastName;
    },
    lastName(value){
        this.fullName = this.firstName + " " + value;
    }
}

```

### <ins> Use computed properties when</ins>

<ol>
  <li>
    You need to compose new data from existing data sources.

    computed:{
       fullName(){
        return `${this.firstName} ${this.lastName}`
       }
    }
   
  </li>
  <li>
    You need to reduce the length of a variable.

    computed:{
       someDeeplyNestedProperty (){
        return this.someProperty
                    .someNestedProperty
                    .someDeeplyNestedProperty;
       }
    }
  </li>
</ol>

### <ins> Use watchers when</ins>

<ol>
  <li>
    You have to check if a property that has changed to a favourable value to know if you're ready to perform an action.
    
    watch: {
    volume(newValue, oldValue) {
      if (newValue > oldValue && newValue === 16) {
        alert(
          "Listening to a high volume for a long time may damage your hearing"
        );
      }
     },
    },
  
   
  </li>
  <li>
    You have to call an API in response to change in application data.
  </li>
  <li>You have to apply transitions.</li>
</ol>
