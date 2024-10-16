# React

## useReducer

### 使用useReducer的一个列子

```react
import React, { useReducer } from 'react';
import ReactDOM from 'react-dom/client';

// 定义初始状态
const initialState = { count: 0 };

// 定义 reducer 函数
const reducer = (state, action) => {
    switch (action.type) {
        case 'increment':
            return { count: state.count + 1 }; // 增加计数
        case 'decrement':
            return { count: state.count - 1 }; // 减少计数
        case 'reset':
            return initialState; // 重置计数
        default:
            throw new Error(`Unknown action type: ${action.type}`); // 错误处理
    }
};

const Counter = () => {
    // 使用 useReducer Hook
    const [state, dispatch] = useReducer(reducer, initialState);

    return (
        <div>
            <h1>Count: {state.count}</h1>
            <button onClick={() => dispatch({ type: 'increment' })}>增加</button>
            <button onClick={() => dispatch({ type: 'decrement' })}>减少</button>
            <button onClick={() => dispatch({ type: 'reset' })}>重置</button>
        </div>
    );
};

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Counter />);
```

```react
const rerender = React.useReducer(() => ({}), {})[1]
```
