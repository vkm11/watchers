# Watchers:-

 - Allow you to watch any data or computed property and execute some code in response to change in the value.
 - Ex:-
 - - implement a volume tracker.
 - - see the current valume.
 - - increase or decrease the volume level.
## Watchers vs Computed Properties
#### Can I use watchers instead of computed properties?
- yes Watchers simply provide a more generic way to react to data changes
- However, it is not recommended to mimic a computed property as a watcher.

## Use Computed properties when
1. you need to compose new data from existing data sources
 
  computed: {
   fullName(){
     return `$(this.firstName) $ this.lastName)`
   }
  }
  
2. You need to reduce the length of a variable

 computed: {
  someDeeplyNestedProperty(){
  return this.someProperty
             .someNestedProperty
             .someDeeplyNestedProperty
  }
}



3. you have to check if a property has changed to a favorable value to know if you're ready to perform an action.

  watch: {
   volume(newValue, oldValue){
    if(newValue > oldValue  && newValue === 16){
     alert(
     `Listening to a high volume for a long time may damage your hearing'
     )
    }
   }
  }
 
 
 
4.You have to call an API in response to change in appliction data.

5. You have to apply transitions.
