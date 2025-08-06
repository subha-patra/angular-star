# ⭐ Angular Star

A lightweight and customizable **star rating** component for Angular 20+. Supports decimal ratings, hover interactions, read-only mode, and full accessibility.

> ✅ Supports Angular 20+  
> 🔧 Fully customizable   
> 🧪 Easy to test and maintain

---

![Star Rating Demo](https://raw.githubusercontent.com/subha-patra/angular-star/refs/heads/main/angular-star.gif)

[Demo](https://stackblitz.com/edit/stackblitz-starters-fx2gszmz?file=package.json)
---
## 📦 Installation

```bash
npm install angular-star
```
--- 

## Usage


Component Setup

```bash
import { AngularStar, starType } from 'angular-star';

@Component({
  imports: [...others, AngularStar]
})

export class <ComponentName> {
  protected config = signal<starType>({ length: 5 });
}

```

Template Example
```bash 
<!-- With Event Binding -->
<angular-star [config]="config()" (getValue)="onGetValue($event)"></angular-star>

```

--- 


## ⚙️ Inputs/Outputs

 | Option            | Type                      |required     | Description                    | Default|
|-------------------|---------------------------|-------------|----------------------------------|---------|
| `getValue`        | `Output`                  |    Yes      | Emits the rating value on change | —    | 
| `config`          | `object`                  |    Yes      | Configuration object (see below) | `{ length: 5 }` |



## ⚙️ Config Options


 | Option            | Type                      |required    | Description                    | Default|
|-------------------|---------------------------|-------------|-------------------------------|---------|
| `length`          | `number`                  |    Yes      | Total number of stars         | 5       |
| `value`           | `number`                  |    No       | Default rating value          | 0       |
| `color`           | `string`                  |    No       | Custom color for all stars (overrides others)| — |
| `badColor`        | `string`                  |    No       | Color for low (bad) ratings   | `#f20808` |
| `avgColor`        | `string`                  |    No       | Color for average ratings     | `#f39c12` |
| `goodColor`       | `string`                  |    No       | Color for high (good) ratings | `#3df400` |
| `spaceBetween`    | `string` or `number`      |    No       | Space between stars           | `0`       |
| `icon`            | `string`                  |    No       | HTML entity or icon used as star symbol   | `&#9733;` | 


---



### 📘 Option Descriptions

- **`length`**: Sets how many stars are displayed.
- **`value`**: Displays an initial rating value.
- **`color`**: Overrides all color settings with a single custom color.
- **`badColor`**: Color for low ratings.
- **`avgColor`**: Color for average ratings.
- **`goodColor`**: Color for high ratings.
- **`spaceBetween`**: Space between individual stars (e.g., 4px, 0.5rem, or a number).
- **`icon`**: Custom icon (HTML entity or text) for the stars. Defaults to a solid star.

--- 

## 📄 License

[![License: MIT](https://raw.githubusercontent.com/subha-patra/angular-star/2c845b1a46d7f60a3a7b94c578a865d576c042e5/licence.svg)](LICENSE)
![npm](https://img.shields.io/npm/v/angular-star)
![npm](https://img.shields.io/npm/dt/angular-star)
![GitHub issues](https://img.shields.io/github/issues/subha-patra/angular-star)
![GitHub stars](https://img.shields.io/github/stars/subha-patra/angular-star)
![GitHub license](https://img.shields.io/github/license/subha-patra/angular-star)
