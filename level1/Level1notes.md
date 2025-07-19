## 1. What is React? (SPA, Components, Virtual DOM)
React ek JavaScript library hai jo UI (user interface) banane ke kaam aati hai.

SPA (Single Page Application): Puri website ek single page pe load hoti hai, pages baar-baar reload nahi hote.

Components: React chhote-chhote blocks (components) ka group hai. Har chhoti functionality ek component hoti hai.

Virtual DOM: React asli DOM pe directly kaam nahi karta. Pehle ek virtual DOM me changes karta hai, fir real DOM me sirf wahi changes karta hai – isse fast ban jaata hai.

## 2. JSX (JavaScript + XML)
JSX ek tarika hai jisse hum JavaScript me HTML jaisa code likh sakte hain.

const element = <h1>Hello World</h1>;
Browser isse samajh nahi sakta, isliye React ke tools ise JS me convert kar dete hain.

## 3. Components (Functional & Arrow Functions)
Functional Component: Simple function jaisa hota hai.

function Greet() {
  return <h1>Hello</h1>;
}
Arrow Function Component:

const Greet = () => <h1>Hello</h1>;
Dono same kaam karte hain – ek component bana ke HTML return karte hain.

## 4. Props (Passing data to components)
Props ka matlab hota hai "properties". Ye data hota hai jo parent component se child ko diya jata hai.

function Greet(props) {
  return <h1>Hello {props.name}</h1>;
}
## 5. useState Hook (State in functional components)
State ka matlab hai component ke andar data store karna jo change ho sakta hai.

useState() ek React ka hook hai jisse functional components me state banate hain.

const [count, setCount] = useState(0);
## 6. Event Handling in React
Jaise button click karne pe kuch karna ho, to event handle karte hain:

function handleClick() {
  alert('Clicked!');
}
<button onClick={handleClick}>Click</button>

 ## 7. Handling Inputs & Buttons
Input ka value track karne ke liye state use karte hain:

const [name, setName] = useState('');
<input type="text" value={name} onChange={(e) => setName(e.target.value)} />

 ## 8. Basic Styling in React (CSS + inline)
2 tarike hote hain:
CSS file import karke
Inline style:

const style = { color: 'red', fontSize: '20px' };
<h1 style={style}>Styled Heading</h1>

## 9. Lists & Keys (looping with .map())
List show karne ke liye .map() lagate hain:

const names = ['A', 'B', 'C'];
names.map((item, index) => <p key={index}>{item}</p>);

## 10. Conditional Rendering (if, ? :, &&)
Kisi condition pe kuch show karna:

{isLoggedIn ? <p>Welcome</p> : <p>Please login</p>}
{isAdmin && <p>Admin Access</p>}
