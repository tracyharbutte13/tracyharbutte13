X

Introduction to graph algorithms

GPT-4.1

html

<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="utf-8" />

<title>VOLTIX Market Portal</tit

<meta name="viewport" content="w

</head>

<body style="background: #111;">

<div id="root"></div>

</body>

</html>

VOLTIX-Market-Portal/frontend/src/App.js

jsx

import React, { useState, useEffect

import QRCode from "qrcode.react";

import AdminLogin from "./AdminLogir


const darkStyle = {

background: "#111",

color: "#e0e0e0",

minHeight: "100vh",

padding: 40px",

fontFamily: "monospace"

};

function App() {

const [market, setMarket)] = useSta

const [quantity, setQuantity] = us

const [qrValue, setQrValue] = uses

useEffect(() => {

fetch("http://localhost:4000/api

.then(res => res.json())

.then(setMarket);

}, []);

const handleOrder = async (type) =

const res await fetch("http://

method: "POST",

headers:

"Content-Type": "ap

hody ISON rinnifv tune

// QR for Cash App (edit logic f const paymentString cashapp:/setQrValue(paymentString);

};

return (

<div style=(darkStyle}>

<h2 style={{ color: "#49fcbc"

<p>Circulating Supply: <b styl

<p>Current Price: <b style={{ {qrValue && (

<input type="number" value={qu <button onClick={() => handled

<button onClick={() => handled

<div>

<h4 style={{ color: "#f8e7

<QRCod 'alue={qrValue) si

<114 style=1100101.

<QRCode value={qrValue) si

</div>

)}

<hr style={{ margin: 40px 0",

<AdminLogin />

</div>

);

}

export default App:

import React, { useState } from "rea import axios from "axios"; import { Widget, addResponseMessage

import "react-chat-widget/lib/styles

const darkStyle = {

background:

"#222",

color:

"#eθεθεθ"

minHeight: "60vh",

padding: "20px",

borderRadius:px",

borderRadius: "12px",

margin: "auto",

maxWidth:

480,

boxShadow: "0 0 12px #49fcbc"

};

export default function AdminLogin()

const [step, setStep] useState(1

const [username, setUsername] = us

const [password, setPassword] = us

const [token, setToken] = useState

const [twoFAQR, setTwoFAQR] = uses

const [code, setCode] useState("

const [adminToken, setAdminToken]

const [error, setError] = useState

// Chatbot

const handleNe serMessage asvno

const res = await axios.post addResponseMessage(res.data.resp };

React.useEffect(() => {

addResponseMessage("Welcome to t // eslint-disable-next-line }, []);

const submitLogin async () => {

setError("");

try {

const res await axios.post(" username, password });

setToken(res.data.token);

setTwoFAQR(res.data.twoFAQR);

setStep(2);

} catch (e) {

setError(e.response?.data?.err

}

};

const submit2FA async () => {

setError("");

try {

const res await axios.post("

token, code

});

setAdminToken(res.data.adminTo

setStep(3);

} catch (e) {

setError(e.response?.data?.err

};

return (

<div style={darkStyle}>

<h1 style={{ color: "#49fcbc"

{step === 1 && (

<>

<input

style={{ margin: 8, colc

placeholder="Username"

value={username}

disabled

/>

<input

style={{ margin: 8, colc

type="password"

placeholder="Password"

valı password}

onchange={e => setrasswo

/>

<button style={{ margin: E

onClick={submitLogin)>

Login

</button>

{error && <div style={{ cc

</>

)}

{step === 2 && (

<>

<div>

<h3 style={{ color: "#f8

{twoFAQR && <img src={tw

</div>

<input

style={{ margin: 8, colc

placlder="Enter 2FA C

Boost 6:30

上

44%

X

Introduction to graph algorithms

GPT-4.1

subtitle="Ask for login help

senderPlaceHolder="Type your

profileAvatar=""

/>

</div>

);

}

4. How to Run and Zip

1. Backend

cd backend

npm install

node index.js

2.

Frontend

4. How to Run and Zip

1. Backend

. cd backend

npm install

node index.js

2. Frontend

cd frontend

npm install

npm start

3. Zip the Repo

From the parent directory: zip -r

VOLTIX-Market-Portal.zip

VOLTIX-Marke ortal/
