# Custome themes: Bootstrap

### Let's create our own theme of Bootstrap instead of using default theme.

```bash
$ mkdir themes
```
```bash
$ touch index.html
```
```bash
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Custom Bootstrap Theme</title>
  </head>
  <body>
    <div>
      <h2>Warning: Custom Styling Ahead!</h2>
      <p>This card uses a fully custom Bootstrap theme.</p>
      <button>Click Me</button>
      <button class="button">Primary Button</button>
      <button class="button button--secondary">Secondary Button</button>
    </div>
  </body>
</html>
```

#### Install Bootstrap

```bash
$ npm init -y
$ npm install bootstrap
```

```bash
$ mkdir scss
```

```bash
$ touch _variables.scss _custom.scss _buttons.scss styles.scss
```

**The styles.scss is the main file of scss**

```bash
// styles.scss
@import "variables";
@import "custom";
@import "buttons";  
```

**_variables.scss**

```bash
// _variables.scss
$primary: #ff5733; 
$secondary: #33ff57;
$danger: #c90606;
$dark: #1e293b;
$light: #dadbdc;
$gray: #b0a7a7;

// Import Bootstrap with our custom variables
@import "../node_modules/bootstrap/scss/bootstrap";
```
**_custom.scss**

```bash
body{
    background-color: $gray;
}
div {
    background-color: $light;
    padding: 1.5rem;
    border-radius: 1rem;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }

  h2 {
    color: $danger;
    font-size: 1.5rem;
    font-weight: bold;
  }
  
  button{
    background-color: $primary;
    color: white;
    padding: 0.5rem 1rem;
    border-radius: 0.5rem;
    transition: background-color 0.3s;
    
    &:hover {
      background-color: darken($primary, 10%);
    }
  }
```
**_buttons.scss**

```bash
$primary-color: #007bff;
$secondary-color: #6c757d;
$font-size: 16px;

@mixin button-styles {
  padding: 10px 20px;
  font-size: $font-size;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.button {
  @include button-styles;
  background-color: $primary-color;
  color: white;

  &:hover {
    background-color: darken($primary-color, 10%);
  }

  &--secondary {
    background-color: $secondary-color;

    &:hover {
      background-color: darken($secondary-color, 10%);
    }
  }
}
```

**Run the following command to proceed to generate output file**

```bash
npx sass scss/styles.scss css/styles.css
```
**The two files are created after run the above command**

* css/styles.css
* css/styles.css.map

**Add the file in HTML file**

```bash
<link href="css/styles.css" rel="stylesheet" />
```

**Output**

![Screenshot from 2025-02-11 04-41-23](https://github.com/user-attachments/assets/bcba3d54-42c5-4480-8001-33ebdcd1cd5d)

