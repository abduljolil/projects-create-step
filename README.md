#  I used this step my projects
# Frontend-used
## 1.React
npm create vite@latest name-of-your-project -- --template react
npm install react-router-dom localforage match-sorter sort-by
## 2.Tailwind
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
### used tailwind.config.js file
content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  ### used index.css file
@tailwind base;
@tailwind components;
@tailwind utilities;
## 3.Daisy UI
npm i -D daisyui@latest
### used tailwind.config.js file
plugins: [require("daisyui")],
### used .eslintrs.cjs
 env: { browser: true, node:true, es2020: true },
 ## Input Form used
 npm install react-hook-form
 ### Example
 import { useForm } from "react-hook-form"

export default function App() {
  const {
    register,
    handleSubmit,
    watch,
    formState: { errors },
  } = useForm()

  const onSubmit = (data) => console.log(data)

  console.log(watch("example")) // watch input value by passing the name of it

  return (
    /* "handleSubmit" will validate your inputs before invoking "onSubmit" */
    <form onSubmit={handleSubmit(onSubmit)}>
      {/* register your input into the hook by invoking the "register" function */}
      <input defaultValue="test" {...register("example")} />

      {/* include validation with required or other standard HTML validation rules */}
      <input {...register("exampleRequired", { required: true })} />
      {/* errors will return when field validation fails  */}
      {errors.exampleRequired && <span>This field is required</span>}

      <input type="submit" />
    </form>
  )
}
