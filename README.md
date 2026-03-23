# 🍔 Burger Blast - Advanced CSS Hero Section

Course: [Web Development 1]
Author: [Abdulrahman Hamdan]
Assignment Value: 15% of final grade

📖 Project Overview
This project is a responsive hero section for a fictional fast-food restaurant called "Burger Blast." The objective of this assignment is to combine advanced layout techniques—specifically CSS Grid, Flexbox, Responsive Images, and the CSS order property—into a single, cohesive, and visually appealing design.
The layout adapts flawlessly from mobile devices up to large desktop screens using a mobile-first approach.

✅ Grading Rubric Checklist & Explanations
Here is a detailed breakdown of how this project meets the specific grading criteria:

1. Folder Setup & Naming (1 Mark)
The project follows standard web development best practices for folder structure and file naming. All files are lowercase with no spaces.
css/ directory contains grid.css (the provided framework) and main.css (custom styles).
images/ directory contains properly optimized images for different viewports.
index.html is kept at the root directory.

2. Properly Submitted via GitHub (3 Marks)
The project was built using proper Git versioning. Commits were made logically as features were added (e.g., "Setup initial HTML structure", "Added Flexbox layout", "Implemented CSS order property").

3. Valid HTML and CSS (2 Marks)
HTML: The markup is semantic, clean, and properly indented. No deprecated tags are used.
CSS: The custom CSS (main.css) is kept simple and highly readable, avoiding overly complex selectors, and seamlessly integrates with the provided grid.css framework.

4. Document Outline (1 Mark)
A perfect document outline is maintained using semantic HTML5 elements:
A <header> tag containing an <h1> is included at the top of the <body>. It utilizes the .visually-hidden utility class from grid.css to hide it from sighted users while keeping it accessible for screen readers and search engines.
The hero content uses <h2> for the main headline and <h3> for the nested grid perks, creating a logical, cascading heading structure.

5. Layout Techniques (8 Marks)
This section forms the core of the assignment. All four required techniques were successfully implemented:

📐 FlexBox
Where to find it: css/main.css under .hero-text.
How it works: The text container uses display: flex; with flex-direction: column; to stack the heading, paragraph, nested grid, and call-to-action button vertically. justify-content: center; and gap: 20px; are used to space the elements perfectly alongside the adjacent image.

🔲 Nested Grid
Where to find it: css/main.css under .nested-perks-grid.
How it works: Inside the main CSS Grid layout (grid-con), there is a nested grid that displays the restaurant "perks" (100% Real Beef, 24/7 Delivery). It uses display: grid; and grid-template-columns: 1fr 1fr; to create two perfectly equal columns inside the text container.

🖼️ Responsive Image
Where to find it: index.html inside the .hero-image container.
How it works: The <picture> element is used to serve the most appropriately sized image based on the user's device screen, saving bandwidth and improving load times.
Desktop screens (1200px+) receive the desktop image.
Tablet screens (768px+) receive the tablet image.
Mobile screens (default) receive the mobile image via the standard <img> fallback.

🔄 CSS Order Property
Where to find it: css/main.css inside the .hero-text, .hero-image, and tablet @media query.
How it works:
In the HTML source order: The text container comes first, and the image comes second.
On Mobile (Mobile-first CSS): We want the image to appear at the top. The CSS applies order: 1; to the .hero-image and order: 2; to the .hero-text.
On Tablet/Desktop (Media Query): Once the screen reaches 768px, the elements are placed side-by-side. The media query updates .hero-text to order: 1; and .hero-image to order: 2;, restoring their natural visual layout (text on the left, image on the right) without ever changing the HTML structure.

📂 Project Structure
code
Text
├── css/
│   ├── grid.css           # Provided grid framework
│   └── main.css           # Custom CSS featuring Flexbox, Grid, and Order
├── images/
│   ├── burger-mobile.jpg  # Mobile optimized image
│   ├── burger-tablet.jpg  # Tablet optimized image
│   └── burger-desktop.jpg # Desktop optimized image
├── index.html             # Main HTML document
└── README.md              # Project documentation

🚀 How to Run the Project
Clone this repository to your local machine.
Open index.html in any modern web browser (Chrome, Firefox, Safari, Edge).
Resize your browser window to see the responsive <picture> tags change and the order property swap the layout from a mobile stack to a side-by-side desktop view.