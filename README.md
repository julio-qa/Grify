
# Grify

**Simple is better**  
Grify is a library that encapsulates ECharts to create dynamic charts using direct data, CSV, or fake data.

Project homepage: [https://github.com/julio-qa/Grify]

---

## 🚀 Features

- **Dynamic Charts**: Create interactive charts like bar, line, pie, and more.
- **CSV Support**: Load data from CSV files and automatically generate charts.
- **Fake Data Generation**: Use Faker.js to quickly prototype with generated data.
- **ECharts Encapsulation**: Simplifies ECharts for easier usage.

---

## 🔧 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/julio-qa/grify.git
   cd grify
   ```

2. Add the necessary scripts to your HTML project:

   ```html
   <script src="https://cdnjs.cloudflare.com/ajax/libs/echarts/5.4.0/echarts.min.js"></script>
   <script src="https://cdnjs.cloudflare.com/ajax/libs/PapaParse/5.4.0/papaparse.min.js"></script>
   <script src="https://cdn.jsdelivr.net/npm/@faker-js/faker/umd/faker.min.js"></script>
   <script src="grify.js"></script>
   ```

---

## 📖 Usage

### Example 1: Chart with Direct Data

   ```javascript
   const directData = [
       ['Category', 'Access', 'Errors'],
       ['A', 10, 20],
       ['B', 15, 25],
       ['C', 20, 30],
   ];

   Grify.loadChart('chart-1', directData, {
       title: 'Chart with Direct Data',
       seriesType: ['bar', 'line'], // Supports different types
   });
   ```

### Example 2: Chart with CSV

   ```javascript
   fetch('data.csv')
       .then(response => response.text())
       .then(csvData => {
           Grify.loadChart('chart-2', csvData, {
               title: 'Chart with CSV',
               seriesType: ['line', 'bar'],
           }, true);
       });
   ```

### Example 3: Chart with Fake Data

   ```javascript
   Grify.generateChartWithFakeData('chart-3', {
       title: 'Chart with Fake Data',
       seriesType: 'pie',
   }, 5, 2);
   ```

---

## 📁 Repository Structure

- **grify.js**: Main library file.
- **examples/**: Example projects using the library.
- **data/**: Sample CSV files.

---

## 🛠️ Built With

- [ECharts](https://echarts.apache.org/en/index.html): For chart rendering.
- [PapaParse](https://www.papaparse.com/): For CSV reading and processing.
- [Faker.js](https://fakerjs.dev/): For fake data generation.

---

## 📝 License

This project is licensed under the [MIT License](LICENSE).

---

## 👥 Contributing

Contributions are welcome! Feel free to open issues, submit pull requests, or suggest improvements.

1. Fork the repository.
2. Create your branch:
   ```bash
   git checkout -b feature/your-feature
   ```
3. Commit your changes:
   ```bash
   git commit -m "Added a new feature"
   git push origin feature/your-feature
   ```

---

## 🌐 Useful Links

- **Official ECharts Documentation**: [https://echarts.apache.org](https://echarts.apache.org)
- **PapaParse**: [https://www.papaparse.com/](https://www.papaparse.com/)
- **Faker.js**: [https://fakerjs.dev/](https://fakerjs.dev/)

---
