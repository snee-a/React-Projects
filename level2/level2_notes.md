## 1. useEffect Hook

Kya karta hai?
useEffect() React ka ek hook hai jo side effects handle karta hai — jaise API call, DOM update, ya localStorage se data lena.

Kab chalega?

useEffect(() => {...}, []) ⇒ sirf 1 baar chalega component ke mount hone pe (like componentDidMount)

useEffect(() => {...}, [count]) ⇒ chalega jab count value change ho

useEffect(() => {...}) ⇒ har render pe chalega

Example:

useEffect(() => {
  console.log("Component loaded");
}, []);

 ## 2. Fetch API
Kya karta hai?
Ye JavaScript ka method hai jo kisi URL se data fetch karta hai.

React me use kaise karein?
Mostly useEffect ke andar use hota hai.

Example:

useEffect(() => {
  fetch("https://api.example.com/data")
    .then(res => res.json())
    .then(data => setData(data));
}, []);

## 3. React Router
Kya karta hai?
Multiple pages banane ke liye use hota hai bina page reload ke.

Important cheezein:

<BrowserRouter> ⇒ app ko wrap karta hai

<Routes> & <Route> ⇒ routes define karte hain

useNavigate() ⇒ programmatically route change karne ke liye

useParams() ⇒ URL parameters ko read karne ke liye

Example:

<Route path="/home" element={<Home />} />

## 4. Forms in React
Controlled vs Uncontrolled Forms:

Controlled: Input ki value React state me hoti hai.

Uncontrolled: Direct DOM se data lete hain (rare in React).

Example:

jsx
Copy
Edit
const [name, setName] = useState("");
<input value={name} onChange={(e) => setName(e.target.value)} />

## 5. Form Validation
Kya hota hai?
Form submit karne se pehle check karna ki input valid hai ya nahi.

Types:

Manual (with if-else)

Libraries: Formik, Yup, React Hook Form

Simple Example:

if (email === "") alert("Email required");

## 6. Lifting State Up
Kya hota hai?
Jab 2 components same state ko use karna chahte hain, toh state parent component me le jaate hain.

Example:

Parent: App.js

Children: Input.js, Display.js

State App me hogi, dono child props se use karenge

## 7. Props Drilling
Kya hota hai?
Jab ek deeply nested component ko data bhejna ho aur bich ke components sirf props pass karte hain.

Problem:
Confusing ho jaata hai agar bahut layers ho.

Solution:
React Context API

## 8. Reusable Components
Kya hota hai?
Aise components jo multiple jagah use ho sakein.

Example:

Button, Card, InputBox — har jagah same design ke sath use ho sakein

## 9. React Fragments
Kya karta hai?
Bina extra <div> ke multiple JSX elements return karne deta hai.

Syntax:

<>
  <h1>Hello</h1>
  <p>World</p>
</>

## 10. Conditional Rendering
Kya karta hai?
Kisi condition ke basis pe component dikhata ya nahi dikhata.

Example:

{isLoggedIn ? <Dashboard /> : <Login />}

## 11. State vs Props
Feature	State	Props
Changeable?	Yes	No
Ownership	Component itself	Passed from parent
Purpose	Internal data	Data communication

## 12. LocalStorage
Kya karta hai?
Browser me data save karta hai jo refresh pe bhi nahi jaata.

Use case:
Save token, theme, user data, etc.

Example:

localStorage.setItem("name", "Sneha");
const name = localStorage.getItem("name");
