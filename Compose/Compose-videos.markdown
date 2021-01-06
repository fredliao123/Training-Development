[Video](https://www.youtube.com/watch?v=VsStyq4Lzxo)

##Key points
- All the architectures MVP, MVVM, MVI are just to help you define your data flow.
- What is the source of truth?
- Who owns it?
- Who can change it?
- Old UI toolkit doesn't answer these questions nicely, because view has it's own state and listeners
- We need a simgle source of truth. Data should always be pass down to children from parents. Children should never read data from a global datastore
- What is compose: a new set of UI widgets; a kotlin compiler plugin; fully compatiable with existing code