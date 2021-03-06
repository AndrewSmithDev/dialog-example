A very simple confirm dialog using the new [dialog element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dialog)

```javascript
export const MyComponent = () => {
  const { confirm } = useConfirm();
  const [message, setMessage] = useState("");

  const handleClick = async () => {
    setMessage("");

    if (await confirm("Are you sure?")) {
      setMessage("✅ You clicked confirm");
    } else {
      setMessage("❌ You clicked cancel");
    }
  };

  return (
    <div>
      <button onClick={handleClick}>Click me</button>
      <p>{message}</p>
    </div>
  );
};

```

[View an running example on Vercel](https://dialog-example-pink.vercel.app/)