# Redux Deep Dive
***Taking A Closer Look***

- Handling **Async Tasks** With Redux
- Where To **Put Your Code**
- **The Redux DevTools**

**Side Effects, Async Tasks & Redux**

Reducers must be ***pure, side-effect free, synchronous*** functions!

***Where should side-effects & async tasks be executed?***

→ Inside the ***components*** (e.g., via useEffects())

→ Inside the ***action creators***

[Frontend Code Depends on Backend Code](https://www.canva.com/design/DAGUUwAmyhQ/XumdVlNxnzY1425rxmPiLA/view?utm_content=DAGUUwAmyhQ&utm_campaign=designshare&utm_medium=link&utm_source=editor)

**Fat Reducers vs Fat Components vs Fat Actions**

Where should your ***logic*** (=code) go?

**Synchronous, side-effect free code**

(i.e. data transformations)

- ***Prefer*** reducers
- ***Avoid*** action creators or components

**Async code or code with side-effects**

- ***Prefer*** action creators or components
- ***Never use reducers!***

**A Problem with useEffect()**

We face one problem when using useEffect the way we currently do it: It will execute when our app starts.

Why is this an issue?

It's a problem because this will send the initial (i.e. empty) cart to our backend and overwrite any data stored there.

**What is a “Thunk”?**

**Thunk**: A function that ***delays an action*** until later.

An action creator function that does ***NOT return the action itself*** 

but instead ***another function*** which ***eventually*** returns the action.

**The Redux DevTools**

https://github.com/reduxjs/redux-devtools

[Redux DevTools - Chrome Web Store](https://chromewebstore.google.com/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd)
