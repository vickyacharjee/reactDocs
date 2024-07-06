# Render in React
## Automatic Re-Rendering

Whenever a state variable updates, React re-renders the component to reflect the changes.

### Example

```jsx
import React, {useState} from 'react'; 

/**
 * A simple counter component that demonstrates automatic re-rendering.
 */
function Counter() {
  const [count, setCount] = useState(0);

  /**
   * Increment the count when the button is clicked.
   */
  const handleClick = () => {
    setCount(count + 1);
  };

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={handleClick}>Increment</button>
    </div>
  );
}