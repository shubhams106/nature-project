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


import React, { useState } from "react";

const App = () =>{
    const [state, setState] = useState({ name: '', class: '' });
    const [array, setArray] = useState([]);

    const onInputChange = (key, value) => {
      setState({
        ...state,
        [key]: value
      })
    }
    console.log("state", state);

    const onServe = () => {
        setArray([...array, state]);
      };
    console.log(array);
    return(
        
            <label>
                name:<input type="text" name="name" onChange={(e) => onInputChange("name", e.target.value)} /> <br/>
                class:<input type="text" name="class" onChange={(e) => onInputChange("class", e.target.value)}/><br/>
                password:<input type="password" name="password" /><br/>
                {/* <button onClick={() => setState({ ...state, name: "name"})}>
                    Click me
                </button> */}
                <button onClick={onServe}>HHH</button>
            </label>
        
    )
}

export default App;
