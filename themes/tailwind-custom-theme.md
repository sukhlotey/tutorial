# Custome themes: TailwindCSS 

### Let's create our own custom theme instead of using default TailwindCSS theme.

```bash
$ mkdir themes
```
```bash
$ touch index.html
```
```bash
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Custom Tailwind Theme</title>
</head>
<body>

    <section>
        <div>
            <h2>Custom Tailwind Theme</h2>
            <p>This is a custom theme created by Sukhpreet Singh</p>
            <button>Click Me</button>
        </div>
    </section>

</body>
</html>
```
#### Install TailwindCSS

```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```
**This creates a tailwind.config.js file where you can define your custom theme.**

#### Customize the Tailwind Theme
**Modify the tailwind.config.js file to disable the default theme and define your own custom styles.**

```bash
/** @type {import('tailwindcss').Config} */
export default {
  content: ["./*.html"], // Update paths as per your project structure
  theme: {
    extend: {
      colors: {
        primary: "#ff5733",
        secondary: "#33ff57",
        dark: "#1e293b",
        light: "#f8fafc",
      },
      fontFamily: {
        sans: ["Poppins", "sans-serif"],
        serif: ["Merriweather", "serif"],
      },
      spacing: {
        '128': '32rem',
        '144': '36rem',
      },
      borderRadius: {
        'xl': '1rem',
      }
    },
  },
  corePlugins: {
    preflight: false, // Disable Tailwind's default styles
  },
  plugins: [],
};
```

* This configuration removes Tailwind’s default theme while allowing you to use only your custom styles.
* Preflight is disabled to prevent Tailwind from applying base styles.

#### Create a Separate CSS File for Tailwind
**Instead of using Tailwind's default theme, create a custom-tailwind.css file and import only what you need:**

```bash
@tailwind base;
@tailwind components;
@tailwind utilities;

button {
  @apply bg-primary text-white px-4 py-2 rounded-lg;
}
h2{
    @apply text-danger font-sans;
}
div {
  @apply bg-light p-6 shadow-lg rounded-xl;
}
```

#### Run this command to generate output of CSS file

```bash
npx tailwindcss -i ./custom-tailwind.css -o ./output.css
```

#### Add this file in HTML

```bash
<link href="output.css" rel="stylesheet">
```

**Output:**

![Screenshot from 2025-02-11 04-13-25](https://github.com/user-attachments/assets/97a358d3-b2b5-4827-9d48-a24dc0ddd8d9)
