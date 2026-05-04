# 🧩 Pokemon – Understanding API Fetching

This is a simple web application that retrieves Pokémon data dynamically from an external API.
It is created as a **learning exercise** to understand how APIs work and how JavaScript interacts with external data.

---

## 🌐 Demo

<p align="center">
  <a href="https://ashikmadhu.github.io/Pokemon/">
    <img src="https://img.shields.io/badge/👁️%20View-3333ff?style=for-the-badge&logo=vercel&logoColor=white"/>
  </a>
</p>

---

## 🎯 Purpose

The goal of this implementation is to understand:

* How APIs provide data
* How to fetch data using JavaScript
* How asynchronous operations work
* How to display dynamic data on a webpage

---

## 🧠 What is an API?

An **API (Application Programming Interface)** allows one system to communicate with another.

Instead of storing all data inside the application, we request data from an external source.
In this case, the application uses the **PokeAPI**, which provides structured Pokemon data.

---

## 🔄 How Data is Fetched

### 1. User Input

The user enters a Pokémon name.

---

### 2. API URL Creation

JavaScript creates a request URL based on the input:

```js
https://pokeapi.co/api/v2/pokemon/{pokemonName}
```

Example:

```js
https://pokeapi.co/api/v2/pokemon/pikachu
```

---

### 3. Sending Request

```js
const response = await fetch(url);
```

* Sends a request to the API
* Waits for a response from the server

---

### 4. Converting Response

```js
const data = await response.json();
```

* Converts the response into JSON format
* Makes it usable in JavaScript

---

### 5. Extracting Data

```js
data.name
data.sprites.front_default
data.types
```

---

### 6. Displaying Data

```js
element.textContent = data.name;
```

* Updates the webpage dynamically
* No page reload required

---

## ⚡ Asynchronous Concept

This uses **async/await** to handle API delays:

* Allows waiting for responses
* Keeps code readable
* Prevents blocking execution

---

## ⚠️ Error Handling

```js
if (!response.ok) {
  throw new Error("Pokémon not found");
}
```

Handles invalid inputs safely.

---

## 🔁 Data Flow

User Input → API Request → JSON Response → Data Extraction → UI Update

---




