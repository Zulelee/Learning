## ReactJS Course by Programming with Most


**What is React?**
+ React is a javascript library for building dynamic UI. 
+ We define a webpage by creating small components.
+ Create each component individually and then connect them.

**Creating a React App**
+ To create a new app (using vite): npm create vite@4.1.0
+ Then move to the new project directory: cd project-folder
+ Then run : npm install
+ Open Project in VS code
+ Use the following cmd to run the app: npm run dev

**Overview of Folders and Files in the project**
+ node_modules folder -> all 3rd party libraries and installed here
+ public folder -> public assests like images and videos are stored
+ src folder -> source code is stored
+ index.html ->
+ package.json -> contains info about the project. (dependencies etc)

**Creating a React component**
+ create a new typescript file in src folder (.tsx)
+ 2 ways to create a component: Javascipt Class and functions
+ Using Functions is more popular
+ Use PascalCasing for naming function
+ In the function you need to describe what the UI will look like when the function is used.
+ function Message(){
      // the tag is JSX (Javascript XML)
      return //<h1>Hello</h1>;
  }
+ to use this function to need to export it as well by : export default Message;
+ To add this component in our APP component (which is our main component), in our App.tsx file:
  import Message form './Message';
  function App(){
    return //<div><Message></Message></div>
  }
  export default App;

**Creating components**
+ to install bootstrap cmd: npm i bootstrap@5.2.3
+ A component cannot return more than one element (eg: cannot return both h1 and ul)
+ If we want to return 2 elements together then wrap them in a div and return the div
+ better way is to return the fragment.
+ In javascript the result of (true && 'text') is text and (false && 'text') is false
+ We can reuse of components with different inputs using props or properties.
+ Instead of defining variables inside a component we should be able to pass them as parameters or inputs to the components using props or properties. Similarly for heading and other elements as well in order to make our components reusable.
+ 
