# 📊 Spreadsheet-MVC

## 📝 Overview

This project implements a **spreadsheet application** using the **Model-View-Controller (MVC)** design pattern. It supports dynamic cell updates, calculations based on **formulas**, and efficient management of **dependencies** between cells. The application tracks **non-empty cells** and ensures that formulas are recalculated when dependencies are modified.

## 🎮 How to Use

To interact with the spreadsheet, follow these steps:

1. **Adding a formula** ➕:
   - To add a formula to a cell, simply input it as you would in a standard spreadsheet, for example: `=A1 + B1`.
   - The spreadsheet will automatically update and recalculate the formula when the values of **A1** and **B1** change.

2. **Entering data** 🖊️:
   - You can enter values directly into any cell, such as `10`, `25`, or text like `Hello World!`.

3. **Updating values** 🔄:
   - When you update the value of a cell, dependent cells will automatically update based on their formulas.

4. **Dependencies** 🔗:
   - If a formula references another cell, the program ensures that updates to the referenced cell trigger recalculations in the dependent cells.

## 🔧 How It Works

### **MVC Architecture** 🏗️

- **Model** 🧠: The Model consists of the `DependencyGraph`, `Formula`, and `Cell` classes. It handles the data logic, calculations, and management of dependencies between cells.
  
- **View** 👀: The View represents the user interface, where users input data and view the results of their formulas. The interface could be either a **console-based** interface or a **GUI** depending on your implementation.
  
- **Controller** 🎮: The Controller serves as the intermediary between the Model and View. It processes user inputs from the View, updates the Model, and refreshes the View to reflect any changes.

### **Key Features** ⚙️
- **Dynamic Cell Management** 🔲: The application keeps track of the current value and formula of each cell, updating them when necessary.
- **Formula Calculations** 🧮: Formulas can be entered in cells, which will automatically recalculate when dependent cells are modified.
- **Dependency Graph** 🌐: The app efficiently manages the relationships between cells, ensuring that recalculations occur in the correct order when data changes.
