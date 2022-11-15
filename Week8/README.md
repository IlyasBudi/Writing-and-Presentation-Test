## Writing Test Week 8
### React Context
- Context adalah salah satu State Management yg di khususkan buat React Js serta mengelola state secara global, dapat di gunakan bersama useState Hook untuk berbagai state.

##### Cara Menggunakan React Contex

1.  Buat Sebuah Folder context di dalam folder src dan di dalam folder tersebut terdapat file dengan nama `<AppContext.js>`

        // 1. Import React Library
        import React from "react"

        // 2. Definisikan variable dengan assign value React.createContext()
        export const AppContext = React.createContext()

2.  Lalu beralih ke <App.js> dan jangan lupa ,mengimport Home dan file-file yg kita butuhkan.

3.  Buat sebuah folder components dan di dalamnya ada folder navbar lalu di dalam folder navbar ada file <Navbar.jsx>
- Penggunaan React Context
  - Untuk membuat new context, gunakan fungsi createContext baru React
  - Fungsi createContext mengembalikan a Provider dan a Consumer component..
### React Testing

- React Testing Library adalah seperangkat helpers yang memungkinkan Anda mengetes komponen pada React tanpa bergantung pada detail implementasinya.
- Testing dapat dilakukan dengan menggunakan JEST

- Pendekatan ini membuat refactoring menjadi mudah dan juga mendorong Anda untuk menerapkan best practices untuk aksesbilitas. Mungkin tidak memberikan cara untuk me-render secara “dangkal” pada sebuah komponen tanpa anak, test runner seperti Jest yang memungkinkan Anda melakukan mocking.

##### Install React Testing Library

        npm install --save-dev @testing-library/react

##### Step dari sebuah Testing

- Assert
- Arrange
- Act

##### Testing dibagi menjadi 2:

- Manual Testing
- Automated Testing

##### Alasan mengapa Menggunakan Testing:

1. Aplikasi bebas dari error dan bug

2. Aplikasi berjalan sesuai dengan ekspektasi

3. Meningkatkan kualitas dari sebuah software dan kepuasan pengguna

##### Alasan menggunakan Automated Testing

1. Lebih reliable karena Manual Testing tetap berpotensi adanya kesalahan dan kekeliruan

2. Lebih cepat dan efisien

3. Mudah untuk dimaintain (Review, Edit, dan Add Collection of Tests)

##### Automated Testing terdiri dari :

1. Unit Test
2. End to End Test
3. Integration Test
