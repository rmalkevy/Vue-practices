## Rules
1) Use in the components only getters - not state.
When you will get data from state - you can be surprised that here no any default state.
In some cases you will need to get predefined data. It will be array [] or object {}.
If you always use getters you can define some value if state is empty.

const state = {
  myList: undefined
}

const getters = {
  getMyList: state => state.myList || [],
}

Then if you will use getters in your project instead of state values, you will always know that you will get array or object - not undefind or null.
