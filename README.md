# 💱 Currency Converter

A clean, responsive, and interactive Currency Converter web application built with vanilla HTML, CSS, and JavaScript. It fetches real-time foreign exchange rates and dynamically updates country flags as currencies are selected.

---

## 📌 Note from the Developer

> **Full Disclosure:**  
> I know this project is really basic and a classic beginner project. However, building this from scratch was an intentional and crucial milestone in my frontend development journey. It helped me bridge the gap between theoretical JavaScript concepts and building a functional, real-world application that talks to external services.

---

## 🚀 Key Concepts Learned

Through building and debugging this project, I gained hands-on experience with several core web development fundamentals:

### 1. 🌐 Working with External APIs & Asynchronous JavaScript
- **Fetch API:** Used `fetch()` to make asynchronous HTTP requests to external REST endpoints.
- **Async/Await:** Handled promises cleanly using modern `async/await` syntax instead of callback chains.
- **JSON Parsing:** Parsed and extracted nested exchange rate data from API response payloads (`response.json()`).
- **Real-Time Data Integration:** Connected to the [Fawaz Ahmed Currency API](https://github.com/fawazahmed0/currency-api) for live exchange rates.

### 2. 🧩 Dynamic DOM Manipulation
- **Populating Elements Dynamically:** Iterated over a currency-to-country code mapping dictionary to generate `<option>` elements for both "From" and "To" dropdown lists on the fly.
- **Attributes & State Management:** Programmatically set attributes like `selected`, `value`, and `innerText`.
- **Dynamic Image Source Updates:** Dynamically switched flag icons via the [Flags API](https://flagsapi.com/) whenever a user changes the selected currency.

### 3. 🎯 Event-Driven Programming
- **`change` Event:** Monitored currency dropdown changes to immediately trigger flag updates.
- **`click` & `submit` Handling:** Prevented default form submission using `evt.preventDefault()` to avoid unnecessary page reloads.
- **`load` Event:** Hooked into the window `load` event to fetch and display default rates (USD to INR) immediately when the page opens.

### 4. 🗂️ Data Structures & Mappings
- **Dictionary/Object Lookups:** Utilized a key-value object (`countryList`) in `code.js` to map ISO 4217 currency codes (e.g., `USD`, `INR`, `EUR`) to their corresponding ISO 3166-1 alpha-2 country codes (e.g., `US`, `IN`, `FR`).

### 5. 🛡️ Input Handling & Edge Cases
- Handled empty, zero, or negative number inputs by resetting values to a sensible default (`1`).
- Ensured currency codes match required API formats (case sensitivity handling with `.toLowerCase()`).

### 6. 🎨 CSS Layout & Modern UI Design
- **CSS Flexbox:** Used flex containers for vertical and horizontal centering, as well as alignment of dropdown items and flag icons.
- **Card UI & Form Styling:** Designed clean, focused card containers with subtle borders, border-radii, and cohesive typography.

---

## 🛠️ Tech Stack

- **HTML5:** Semantic structure for converter layout, dropdowns, and input fields.
- **CSS3:** Flexbox layout, responsive sizing, custom form controls, and clean aesthetics.
- **JavaScript (ES6+):** Async/await, Fetch API, DOM manipulation, and event handling.
- **APIs Used:**
  - [Currency API](https://cdn.jsdelivr.net/npm/@fawazahmed0/currency-api@latest/v1/currencies) for live currency conversion rates.
  - [Flags API](https://flagsapi.com/) for country flag icons.

---

## 📂 Project Structure

```text
currency-converter/
│
├── curr.html       # Main HTML markup and structure
├── curr.css        # Stylesheet for layout, cards, and dropdowns
├── code.js         # Currency code to country code mapping
├── curr.js         # Application logic, API integration, and DOM events
└── README.md       # Project documentation and learnings
```

---

## 💻 How to Run Locally

1. **Clone the repository:**
   ```bash
   git clone https://github.com/prabal009/Currency-Converter.git
   ```

2. **Navigate to the project folder:**
   ```bash
   cd Currency-Converter
   ```

3. **Open the project:**
   - Double-click `curr.html` to open it directly in any browser, or
   - Use the **Live Server** extension in VS Code for live reloading.

---

## 🔮 Future Improvements

- [ ] Add a swap/reverse button to quickly switch "From" and "To" currencies.
- [ ] Add loading skeletons/spinners while fetching rates.
- [ ] Implement historical exchange rate charts.
- [ ] Add dark mode support.

---

## 👤 Author

- **Prabal** - [@prabal009](https://github.com/prabal009)
