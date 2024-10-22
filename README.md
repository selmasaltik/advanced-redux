# Redux Deep Dive
***Taking A Closer Look***

- Handling **Async Tasks** With Redux
- Where To **Put Your Code**
- The Redux **DevTools**

**Side Effects, Async Tasks & Redux**

Reducers must be ***pure, side-effect free, synchronous*** functions!

***Where should side-effects & async tasks be executed?***

→ Inside the ***components*** (e.g., via useEffects())

→ Inside the ***action creators***
