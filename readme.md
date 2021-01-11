<center>
<h1>ZHooks</h1>
_More will be added eventually_
</center>

<center>
  <h1>UseConstructor Hook</h1>
</center>

> All Credit to Adam Nathaniel Davis in his post on dev.to -> [constructors in functional components with hooks](https://dev.to/bytebodger/constructors-in-functional-components-with-hooks-280m) with a small tweak by Timo Zimmermann down in the comments

# Usage

```ts
const App = () => {
  useConstructor(() => {
    console.log(
      "This only happens ONCE and it happens BEFORE the initial render."
    );
  });
  const [counter, setCounter] = useState(0);

  return (
    <>
      <div>Counter: {counter}</div>
      <div style={{ marginTop: 20 }}>
        <button onClick={() => setCounter(counter + 1)}>Increment</button>
      </div>
    </>
  );
};
```

> Constructor should be the first line in the function.

- [ ] Build the ts into a js file.....
