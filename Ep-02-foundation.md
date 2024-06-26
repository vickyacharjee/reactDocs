
PART 1
```
import React from "react"
import ReactDOM from "react-dom/client"


// using React Element
const reactElement=React.createElement('h1',{id:"heading"},"Hello From React");

// Same thing via JSX
const jsx=<h1>Hello from JSX</h1>;
/*
    JSX is an transpiller React element
    JSX used a library 'Babel' in order to use as same a like HTML
    Note: JSX is not HTML code but act as same alike

    compliling line: ReactElement
        ReactElement => javaScript[Object]


    compliling line: JSX
        JSX[Babel] => ReactElement => javaScript[Object]
*/ 


//  React Components
//  1- Class Based Components[old]
//  2- Function Based Component Based Components[NEW]
//  3- A function returning soem piece of jsx is functional component
const JsxComponent=()=>{
    return <h1>Hello from inside JSX Functions</h1>;
}

// same thing in different way to declare
// First way
const JsxComponentOne=()=> <h1>Hello from JSX function from singe line</h1>;

// Second Way
const JsxComponentTwo=()=>(
    <h1>Hello from JSX using round braces</h1>
)



const root=ReactDOM.createRoot(document.getElementById('root'));
root.render(JsxComponentTwo());
```





PART 2 
```
import React from "react"
import ReactDOM from "react-dom/client"

// its a good practice and a convention to use the first letter as capital
const Title=()=>(
    <h1>hello from title jsx</h1>
)

// for functional component 
const Title2=()=>(
    <h1>hello from title2 jsx</h1>
)
const Title3=()=>(
    <h1>hello from title3 jsx</h1>
)
// for passing as element
const testName=<span>Yo there from inside element</span>
const name=10// line no. 16 and 24 are embedding js inside jsx
const HeadingComponent=()=>(
    <div id='container'>
        <Title/>
        <h1>hello from functional component</h1>
        <Title2/>
        {/* {Title3()}// The functional component is used or passed as react element like {addOrCall The function here()} */}
        <Title2></Title2> // another way of adding the cmponent and that works the same 
        <Title2/>// This is component 
        {testName}// This is simple react element
       <h3> so the output is {name+112}</h3>
    </div>
)

//   This is done using normal function so here mandatorily we need to use or pass return statement along with () Braces
// const HeadingComponent=function(){
//     return(
//     <div id='container'>
//         <Title/>
//         <h1>hello from functional component</h1>
//         <Title2/>
//         <Title2/>
//     </div>
//     )
// }
const root=ReactDOM.createRoot(document.getElementById('root'));
root.render(<HeadingComponent/>);

NOTE: Component Composition is composing of component inside one another
```
```

```


