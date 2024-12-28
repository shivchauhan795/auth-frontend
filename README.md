# shivchauhan795/auth-frontend
This package includes React components for authentication (login, register) and integrates Tailwind CSS.

Contribute in the Repo: https://github.com/shivchauhan795/auth-frontend

## Installation

1. Install the package:

   ```bash
   npm install @shivchauhan795/auth-frontend
2. Install tailwind.css:
    ```  
   npm install -D tailwindcss postcss autoprefixer
   npx tailwindcss init -p
3. Add this line on the top of the file:
    ```
    import '@shivchauhan795/auth-frontend/index';
3. Add or update postcss.config.css:

    ```bash
    export default {
      plugins: {
        tailwindcss: {},
        autoprefixer: {},
      },
    }

## Run

### For Login:
1. Add this line on Top:

    ```
    import Login from '@shivchauhan795/auth-frontend/login';

2. Add this code for the Login Component:

    ```bash
    <Login
       backendURL="YOUR_BACKEND_URL"    // e.g: http://localhost:3000/login
    />


### For Register:
1. Add this line on Top:

    ```
    import Login from '@shivchauhan795/auth-frontend/register';

2. Add this code for the Login Component:

    ```bash
    <Register
       backendURL="YOUR_BACKEND_URL"    // e.g: http://localhost:3000/login
    />


### Create auth-frontend.d.ts file and add this:

```bash  
declare module '@shivchauhan795/auth-frontend/login';
declare module '@shivchauhan795/auth-frontend/register';
declare module '@shivchauhan795/auth-frontend/index';
```
## How to Use:

- For Register:
```bash
import Register from '@shivchauhan795/auth-frontend/register';
import '@shivchauhan795/auth-frontend/index';

function App() {
  const handleRegisterSuccess = (response) => {
    console.log('Register successful:', response);
  };
  return (
    <>
      <Register
        backendURL="http://localhost:4000/v1/admin/register"
        onSuccess={handleRegisterSuccess}
      />
    </>
  )
}

export default App

```
- For Login:
```bash
import Login from '@shivchauhan795/auth-frontend/login';
import '@shivchauhan795/auth-frontend/index';

function App() {
  const handleLoginSuccess = (data) => {
    console.log('Login successful:', data);
    // You can store tokens, navigate, or trigger other actions here
  };
  return (
    <>
      <Login
        backendURL="http://localhost:4000/v1/admin/login"
        onSuccess={handleLoginSuccess}
      />
    </>
  )
}

export default App

```