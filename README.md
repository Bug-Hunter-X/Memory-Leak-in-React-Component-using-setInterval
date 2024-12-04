# React setInterval Memory Leak
This example demonstrates a common mistake when using setInterval within a React component's useEffect hook.  Forgetting to return a cleanup function from useEffect leads to memory leaks and unexpected behavior after the component unmounts.

The `bug.js` file contains the erroneous code, while `bugSolution.js` provides the corrected version.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console; the memory leak will not be immediately apparent in the browser's dev tools but it will cause problems if you render this component many times.
5. Compare `bug.js` and `bugSolution.js` to understand the correction.