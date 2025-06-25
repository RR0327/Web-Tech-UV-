# <h1 align="center"> Group Budget Splitter </h1>

Absolutely! Here’s a **full-proof, clear explanation** of your project that you can confidently present to your teacher. I’ve broken it down into sections for clarity.

---

# 📝 **Project Explanation: Group Budget Splitter**

---

### 1. **Project Objective**

The goal of this project is to build a web application that helps a group of people fairly split shared expenses, such as rent, food, utilities, etc. The app:

* Accepts multiple expense categories with their amounts.
* Accepts the number of people and how much each person has contributed.
* Calculates how much each person *should* pay equally.
* Shows how much each person overpaid or underpaid.
* Provides payback instructions indicating who owes money to whom and how much.

---

### 2. **Technologies Used**

* **Backend:** Python with the Django framework
* **Frontend:** HTML, CSS, JavaScript (vanilla)
* **Templates:** Django template engine to dynamically render HTML pages
* **Styling:** Custom CSS for professional UI design
* **Data Handling:** Django forms to process user input

---

### 3. **Project Structure**

* `models.py`: Defines data models for `Category`, `Person`, and `Contribution` (though main input is form-based without DB storage in this version).
* `forms.py`: Defines Django forms for categories and persons input.
* `views.py`: Contains the business logic for:

  * Displaying input forms
  * Handling form submissions
  * Performing calculations and payback logic
  * Rendering results.
* `urls.py`: Defines URL routes connecting views.
* `templates/core/`: Contains HTML templates (`home.html` for input and `result.html` for output).
* `static/css/style.css`: Contains the CSS for styling the app.

---

### 4. **How It Works**

* **Input Page (home.html):**
  Users can dynamically add any number of expense categories (e.g., Rent, Food) and persons with the amounts they paid. This is powered by JavaScript to add fields on demand.

* **Calculation (views.py - calculate view):**
  On form submission, the backend:

  1. Totals all category expenses.
  2. Divides total equally among the number of people.
  3. Calculates difference between each person’s paid amount and their share.
  4. Figures out paybacks — who owes whom and how much to balance the expenses.

* **Output Page (result.html):**
  Shows:

  * Breakdown of categories and amounts.
  * Total expense and equal share per person (rounded to 2 decimals for readability).
  * A table listing each person’s paid amount, should pay amount, and difference.
  * A payback instruction list specifying the minimal transfers needed to settle debts.

---

### 5. **Key Features and Professional Aspects**

* **Dynamic form fields:** Users can add multiple categories and persons as needed.
* **Clear financial calculations:** Uses Python’s `Decimal` for precision.
* **Clean, responsive UI:** Simple but professional layout with CSS styling.
* **Decimal formatting:** Outputs financial values rounded to two decimal places for clarity.
* **Extensible architecture:** Modular Django app structure making future enhancements easy.
* **CSRF protection:** Secure form submissions with Django’s CSRF token.
* **Error handling:** Required fields and input types enforced by HTML and forms.

---

### 6. **Possible Extensions**

* Add user authentication and save budgets for logged-in users.
* Store data persistently using Django models.
* Export results as PDF or Excel.
* Add charts/graphs for visual expense summaries.
* Add multi-currency support.

---

### 7. **How to Run the Project**

1. Clone/download the project.
2. Install dependencies (`Django`).
3. Run migrations (if using models):

   ```bash
   python manage.py migrate
   ```
4. Create a superuser (optional for admin):

   ```bash
   python manage.py createsuperuser
   ```
5. Run the development server:

   ```bash
   python manage.py runserver
   ```
6. Visit `http://localhost:8000/` in your browser to use the app.

---

### 8. **Summary**

This Django project demonstrates core web development skills, including backend logic, form handling, templating, and frontend dynamic interactions, applied to a practical and useful tool that simplifies group expense sharing with clear and fair calculations.

---
