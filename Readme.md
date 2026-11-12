## Exp 10 – React Strict Mode
## NAME: LIVYA DHARSHINI G
## REG NO: 2305001013
## Aim
To create a React application using Strict Mode and understand how it helps identify potential
problems and unexpected side effects during development.
## Objectives
1. To understand React Strict Mode.
2. To enable Strict Mode in a React application.
3. To observe the additional development-time checks.
4. To understand the use of useEffect() and cleanup functions.
## Program
```
1. main.jsx

import { StrictMode } from "react";
import { createRoot } from "react-dom/client";
import App from "./App.jsx";
createRoot(document.getElementById("root")).render(
<StrictMode>
<App />
</StrictMode>
);

2. App.jsx

import { useEffect, useState } from "react";
function App() {
const [count, setCount] = useState(0);
useEffect(() => {
console.log("Effect started");
    return () => {
      console.log("Effect cleanup");
    };
  }, []);
  return (
    <div>
      <h1>React Strict Mode</h1>
      <h2>Count: {count}</h2>
      <button onClick={() => setCount(count + 1)}>
        Increase
      </button>
    </div>
  );
}
export default App;
```
## Output
1. React Strict Mode Application

   <img width="551" height="200" alt="image" src="https://github.com/user-attachments/assets/3be099b6-bbbb-417e-aafd-36ccda3a497d" />

3. Browser Console Output

   <img width="1010" height="115" alt="image" src="https://github.com/user-attachments/assets/3381cc3f-73ba-4c60-b4ed-db89b2055c6e" />

## Result
Thus, the React application was successfully executed using Strict Mode. Its development-time
checks and the use of useEffect() cleanup were studied.
