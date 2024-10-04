## Keystroke Coding Dataset for Two Web Programming Problems

### Overview
This dataset captures students' keystroke-level coding behavior during two introductory-level web programming exercises. It was collected during a data collection session designed to simulate a real-time classroom environment. We recruited 22 students from [redacted for anonymity], including 10 beginners, 11 intermediates, and 1 advanced student in web programming.

### Data Collection
The data collection sessions were conducted synchronously via Zoom, with each participant completing the session individually. Participants were given two web programming exercises to complete, each with a 20-minute time limit. A member of the research team monitored the session and collected data using a customized VS Code extension. Participants were permitted to use external resources such as Google and inline GitHub Copilot suggestions, but were restricted from using ChatGPT or other large language models to directly solve the exercises. This setup aimed to balance the realistic use of AI tools in programming while ensuring reliable data for analyzing student progress.

### Dataset Details
The dataset captures every keystroke made by participants, with each student averaging around 810 keystrokes per exercise. The data is stored in InfluxDB, organized with timestamps, participant IDs (anonymized), and details of each edit made. The exercises require building interactive web applications using HTML, CSS, and JavaScript, with descriptions available in the [Appendix](#exercise-descriptions). This level of granularity provides a detailed view of students' coding processes, making the dataset valuable for research on programming education, learning patterns, and problem-solving approaches in programming classes.

### Motivation
Traditional code datasets often lack real-time behavioral data, making it difficult to understand how students approach coding problems and how they solve them. This dataset addresses this gap by providing a comprehensive, real-time view of coding behavior, allowing researchers to analyze student learning trajectories and identify areas of struggle or success at a finer level of detail.

### Dataset Structure
The dataset is structured to show real-time programming progress through a dashboard similar to Codeopticon, making it easier to visualize each student's coding activities chronologically. This structure can serve as a benchmark for future research, enabling studies on coding patterns, problem-solving strategies, and learning progress in programming education.

### Exercises
#### 1. Exercise: Create a To-Do List Webpage
Participants were instructed to create a to-do list webpage using HTML, CSS, and JavaScript. The exercise required creating three files: `index.html`, `script.js`, and `styles.css`. Key tasks included building the HTML structure, adding interactivity for adding and removing items, and styling the page. The exercise focused on fundamental web programming skills, such as DOM manipulation and event handling.

#### 2. Exercise: Create an Image Carousel
Participants were tasked with creating a simple image carousel using HTML, CSS, and JavaScript. The exercise required creating three files: `index.html`, `script.js`, and `styles.css`. Participants needed to implement a gallery of thumbnail images, add interactivity to select images, and style the carousel to ensure a visually appealing layout. The exercise emphasized interactivity and dynamic content manipulation.

For more detailed exercise descriptions, refer to the [Appendix](#exercise-descriptions).

### Usage and Applications
This dataset can be used for various research purposes, including:
- Analyzing coding behavior at the keystroke level.
- Investigating problem-solving strategies in programming.
- Identifying common patterns and mistakes among students at different skill levels.
- Designing and evaluating educational interventions to improve programming pedagogy.

### Appendix: Exercise Descriptions <a id="exercise-descriptions"></a>
Detailed instructions and requirements for the two exercises are provided below. These descriptions outline the specific tasks participants were asked to complete and the expected outcomes for each exercise.

#### Exercise 1: Create a To-Do List Webpage
1. **HTML Structure**:
   - Add a title `<h1>` with the text "Todo List" and ID `#pageTitle`.
   - Create an input box and button inside a `<div>` with the ID `#inputContainer`.
   - Add an empty `<div>` below for displaying the to-do items.

2. **Add Button Interactivity**:
   - Implement functionality to add a new to-do item to the list.
   - Ensure each new item has a text content and a delete button.

3. **Delete Button Interactivity**:
   - Implement functionality to remove a to-do item when the delete button is clicked.

#### Exercise 2: Create an Image Carousel
1. **HTML Structure**:
   - Create a thumbnails section for displaying a series of images.
   - Add a featured image section that shows the selected image and its description.

2. **Thumbnails Generation**:
   - Loop through a provided array of images and dynamically create image elements.
   - Append each image element to the thumbnails container.

3. **Making Images Clickable**:
   - Update the featured image and its description based on the selected thumbnail.
   - Highlight the currently selected image with a red border.

### Contact
For any questions or issues regarding the dataset, please contact [email@example.com].
