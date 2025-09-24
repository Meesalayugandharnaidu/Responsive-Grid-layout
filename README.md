# Resposive-Grid-layout

### **Description**

This project creates a classic, **five-section web page layout** using **CSS Grid** for precise and efficient structure. It features common website components: a Header, Navigation Bar, Main Content, Sidebar (Aside), and Footer. The layout is designed to be **responsive** and maintain a distinct visual separation between its parts.

-----

### **Key Features**

#### **1. Structure (HTML)**

  * **Semantic Divisions:** The HTML file (`index.html`) uses a single main container (`.main`) which holds five primary `div` elements, clearly named to represent their function: `.header`, `.nav` (Navbar), `.content`, `.aside` (Sidebar), and `.footer`.

#### **2. CSS Grid Layout (`style.css`)**

  * **Grid Template Areas:** The core of the design uses the `grid-template-areas` property to define the placement of the sections:
    ```css
    grid-template-areas:
        "header header header"
        "navbar contentArea aside"
        "navbar footer footer";
    ```
    This visually maps the layout into a **3x3 grid**.
  * **Row and Column Sizing:**
      * **Rows (`grid-template-rows`):** The layout is fixed at three rows:
          * Header: `100px` (fixed height)
          * Content/Aside: `1fr` (takes up the remaining available space)
          * Footer: `70px` (fixed height)
      * **Columns (`grid-template-columns`):** The layout is fixed at three columns:
          * Navbar: `1fr`
          * Content: `4fr` (four times wider than the Navbar and Aside)
          * Aside: `1fr`
  * **Full Height:** The `.main` container is set to `height: 100vh` to ensure the grid occupies the full vertical space of the viewport.

#### **3. Component Placement and Styling**

  * **Navbar (Vertical):** The `.nav` (navbar) occupies the first column across **two rows** (`navbar contentArea aside` and `navbar footer footer`), creating a vertical sidebar down the left side.
  * **Header/Footer (Full Width):** The `.header` spans all three columns at the top, and the `.footer` spans the bottom two columns (next to the navbar).
  * **Styling:** All sections share a default `cadetblue` background. The `.content` area is visually distinguished with a semi-transparent blue background (`rgba(0, 0, 255, 0.377)`). All sections have padding, white text, and a `2px solid black` border for clear separation.
