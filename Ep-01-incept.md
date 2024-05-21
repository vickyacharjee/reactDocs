// const root=document.getElementById('root');
        // const heading=document.createElement('h1');
        // heading.innerHTML="Yo world from JavaScript"
        // root.appendChild(heading);
    
        //====using React====
       //  const heading=React.createElement('h1',{id:"heading",class:"classHeading",xyz:"testForPersonalAttribute"},"Hello From React");// creating an element
       //  const root=ReactDOM.createRoot(document.getElementById('root'));// fetching from root div
    
       //  root.render(heading); //simply appending

        // Note:
        // React.createElement('h1',{id:"heading"},"Hello From React");
        // first parameter is which elemen tag u want to create
        // second parameter is object... So here in object we declate the attributes and property like class, ID etc
        // third parameter is giving a content to that element likeWise innerHTML, innerTextContent etc [also know as children]

                       //==== React before JSX ====

       // EXAMPLE:1 
       /*    here we are creating this type of structure via React.createElement()
              <div id="root">
                     <div id="parent">
                            <h1> hi from h1 tag </h1>
                     </div>       
              </div>
       // */
       //  const complex=React.createElement('div',{id:'parent'},
       //                React.createElement('h1',{},"hi from h1 tag"))




       // EXAMPLE:2
       /*    here we are creating this type of structure via React.createElement()
              <div id="root">
                     <div id="parent">
                            <h1> hi from h1 tag </h1>
                            <h2> hi from h2 tag </h2>
                            <h3> hi from h3 tag </h3>
                            <h4> hi from h4 tag </h4>
                            <h5> hi from h5 tag </h5>
                            <h6> hi from h6 tag </h6>
                     </div>       
              </div>
       */               
       //  const complex=React.createElement('div',{id:'parent'},
       //                [React.createElement('h1',{},"hi from h1 tag")],
       //                [React.createElement('h2',{},"hi from h2 tag")],
       //                [React.createElement('h3',{},"hi from h3 tag")],
       //                [React.createElement('h4',{},"hi from h4 tag")],
       //                [React.createElement('h5',{},"hi from h5 tag")],
       //                [React.createElement('h6',{},"hi from h6 tag")]);
        


       // EXAMPLE:3
       /*    here we are creating this type of structure via React.createElement()
              <div id="root">
                     <div id="parent">
                            <h1> hi from h1 tag </h1>
                            <h2> hi from h2 tag </h2>
                            <h3> hi from h3 tag </h3>
                            <h4> hi from h4 tag </h4>
                            <h5> hi from h5 tag </h5>
                            <h6> hi from h6 tag </h6>
                     </div>       

                       <div id="parent">
                            <h1> hi from h1 tag </h1>
                            <h2> hi from h2 tag </h2>
                            <h3> hi from h3 tag </h3>
                            <h4> hi from h4 tag </h4>
                            <h5> hi from h5 tag </h5>
                            <h6> hi from h6 tag </h6>
                     </div>  
              </div>
       */               
        const complex=React.createElement('div',{id:'parent'},
                     [ 
                      React.createElement('div',{id:'child'},
                      [React.createElement('h1',{},"hi from h1 tag")],
                      [React.createElement('h2',{},"hi from h1 tag")],
                      [React.createElement('h3',{},"hi from h1 tag")],
                      [React.createElement('h4',{},"hi from h1 tag")],
                      [React.createElement('h5',{},"hi from h1 tag")],
                      [React.createElement('h6',{},"hi from h1 tag")])],
                      [
                      React.createElement('div',{id:'child'},
                      [React.createElement('h1',{},"hi from h1 tag")],
                      [React.createElement('h2',{},"hi from h1 tag")],
                      [React.createElement('h3',{},"hi from h1 tag")],
                      [React.createElement('h4',{},"hi from h1 tag")],
                      [React.createElement('h5',{},"hi from h1 tag")],
                      [React.createElement('h6',{},"hi from h1 tag")])]);

        const root=ReactDOM.createRoot(document.getElementById('root'));// fetching from root div
        root.render(complex); //simply appending
