# nature-project
const App = () => {
  const [state, setState] = useState({ count: 0, number: 0 });
  const [array, setArray] = useState([]);

  const onServe = () => {
    setArray([...array, state]);
  };
console.log(array);
  return (
    <div>
      <p>u clicked {state.count} times </p>
      {/* <p>u won {number} times </p> */}
      <button onClick={() => setState({ ...state, count: state.count + 1 })}>
        Click me
      </button>
      <button onClick={onServe}>arrayyy!!</button>
      {/* <button onClick={() => setNumber(number + 1)}>winnning streak!!</button> */}
    </div>
  );
};

export default App;
