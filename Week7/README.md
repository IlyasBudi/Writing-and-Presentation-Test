## Writing Test Week 7
### Props-Types
- Prop types merupakan sebuah lib yang dapat membantu kamu untuk memeriksa data props yang kamu kirim agar sesuai dengan ekspektasi. Jika tidak sesuai, maka akan muncul pesan error.
- Install PropTypes
```jsx
Npm install prop-types
```
- Contoh penggunaan Props Types
```jsx
Import PropTypes from “prop-types”;
Function Header(props) {
  Return (
    <>
        <h2> Name: {props.char}</h2>
        <h2>Age: {props.age}</h2>
    </>
  )
}

Header.proptypes = {
    Char: PropTypes.string,
    Age: PropTypes.number
}
```
Props akan dikirim harus sesuai dengan tipe data yang diinginkan. Dengan begitu, kita akan mendapatkan pesan error jika tidak sesuai dengan ekspektasi. Sehingga, jika terjadi kesalahan kita dapat langsung mengetahuinya dan segera diperbaiki.
### React-Router
- React Router merupakan standar routing yang digunakan sebagai library React JS untuk mengarahkan website dari page satu ke page lainnya, dimana page tersebut diarahkan dengan menggunakan URL.
- Installation react-router
```jsx
Npm install react-router-dom
```
- Selanjutnya import librarynya dan bungkus ``<App />`` dengan ``<BrowserRouter>`` di dalam file main.jsx
```jsx
// Main.jsx
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App";
import { BrowserRouter } from "react-router-dom";

ReactDOM.createRoot(document.getElementById("root")).render(
  <React.StrictMode>
    <BrowserRouter>
      <App />
    </BrowserRouter>
  </React.StrictMode>
);
```
- Import library dan beberapa page dan component, kemudian panggil yang sudah di import ke dalam return di file ``App.jsx.
```jsx
return (
    <>
      <nav>
        <Link to={"/"}>Home |</Link>
        <Link to={"/about"}>About</Link>
      </nav>
      <Routes>
        <Route path="/" element={<HomePage />} />
        <Route path=”/” element={<AboutPage /> />
      <Routes>
    </>
);
export default App;
```
##### Params
- Params: Digunakan untuk mengirim data lewat router. Contohnya:
```jsx
import * as React from 'react';
import { Routes, Route, useParams } from 'react-router-dom';

function ProfilePage() {
  // Get the userId param from the URL.
  let { userId } = useParams();
  // ...
}

function App() {
  return (
    <Routes>
      <Route path="users">
        <Route path=":userId" element={<ProfilePage />} />
        <Route path="me" element={...} />
      </Route>
    </Routes>
  );
}
```
##### Nested Route
- React Router menggunakan Nested Route untuk merender informasi yang lebih spesifik di dalam child component. Contohnya:
```jsx
import User from './user/User';
  import Setting from './user/setting/Setting';
  import Profile from './user/profile/Profile';
  import Favorite from './favorite/Favorite';

  function App() {
    return (
      <>
    <ul className='user'>

    <li><Link to="/">Home</Link></li>
    <li><Link to="/user">User</Link></li>
    <li><Link to="/favorite">FavoriteKu</Link></li>
    <li> <Link to="/galeri">Galeri</Link></li>
    </ul>

    <Routes>
          <Route path='/' element={<Home/>}/>
          <Route path='/User' element={<User/>}/>
          <Route path='/Gallery' element={<Gallery/>}/>
          <Route path='/Favorite' element={<Favorite/>}/>

          {/* Nested router */}
          <Route path='/Favorite/Music' element={<Music/>}/>
          <Route path='/User/Profile' element={<Profile/>}/>
          <Route path='/User/Settings' element={<Settings/>}/>
    </Routes>
     </>
    );
  }
```
### React Redux
- Redux adalah salah satu library state management yang menyimpan state di satu tempat, sehingga lebih mudah untuk di manage. Biasanya tanpa state management library, kita akan menyimpan state di setiap komponen. Kalau butuh komunikasi data antar komponen, kita bisa menggunakan props. Namun akan menjadi tantangan bila aplikasi yang kita bangun semakin kompleks. Akan sedikit sulit untuk mengatur state di komponennya, belum lagi jika ada komunikasi data antar komponen. Salah satu solusi dari masalah tersebut adalah dengan menggunakan library state management seperti redux.
- Ada 3 komponen utama dalam redux yaitu:<br />
1. Action<br />
Action berfungsi sebagai penampung data dan juga untuk menentukan jenis aksi apa yang akan dilakukan.<br />
2. Reducer<br />
Reducer merupakan bagian yang menyimpan state state yang akan dipakai nanti. State ini akan menjadi respon ketika action yang dihubungkan ke Reducer ini dipanggil.<br />
3. Store<br />
Store berfungsi untuk menyambungkan antara action dan juga reducer.
### Redux-Thunk
- Redux-Thunk adalah sebuah middleware yang memungkinkan kita memanggil pembuat aksi yang mengembalikan fungsi sebagai ganti objek aksi.
- Redux-Thunk solusi ketika kita menggunakan fetch data dari sebuah External API atau yang memiliki side effect (proses ashynchronous).
- Installation Redux-Thunk
```jsx
npm install redux react-redux redux-thunk
```
