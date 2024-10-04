## Keystroke Coding Dataset

### Overview
This dataset captures students' keystroke-level coding behavior for two introductory-level web programming exercises. It was collected during a data collection session designed to simulate a real-time classroom environment. We recruited 22 students, including 10 beginners, 11 intermediates, and 1 advanced student in web programming, from [redacted for anonymity].

### Dataset Structure

The dataset is organized into the following structure:

- **imageCarousel/**: Contains individual files recording the keystroke data of each student working on the image carousel exercise.
- **todoList/**: Contains individual files recording the keystroke data of each student working on the to-do list exercise.
- **mergedSortedData_image.json**: A merged JSON file that consolidates and sorts all students' keystroke data for the image carousel exercise based on timestamps, assuming all students started at the same time.
- **mergedSortedData_todo.json**: A merged JSON file that consolidates and sorts all students' keystroke data for the to-do list exercise based on timestamps, assuming all students started at the same time.

### Data Collection
The data collection sessions were conducted synchronously via Zoom, with each participant completing their session individually. Each participant was given two web programming exercises to complete, with a 20-minute time limit for each exercise. During the session, a research team member monitored the participants' progress and collected data using a customized VS Code extension. Participants were allowed to use external resources such as Google and inline GitHub Copilot suggestions but were restricted from using ChatGPT or other large language models to obtain direct code answers. This approach aimed to balance the realistic use of AI tools while ensuring reliable data for analyzing student progress.

### Dataset Details
The dataset captures every keystroke made by participants, with each student averaging around 810 keystrokes per exercise. The data is stored in InfluxDB and is organized with timestamps, anonymized participant IDs, and detailed information about each edit. The exercises involve building introductory-level interactive web applications using HTML, CSS, and JavaScript. Descriptions of the exercises are available in the [Appendix](#exercise-descriptions).

### Dataset Motivation
Traditional code datasets often lack real-time behavioral data, making it difficult to understand how students approach coding problems and navigate through challenges. This dataset addresses this gap by providing a detailed view of students' coding processes. By capturing each keystroke, it offers valuable insights into students' problem-solving strategies and learning trajectories, making it suitable for research on programming education.

### Applications
This dataset can be used for various research purposes, including:
- Analyzing coding behavior at a granular level.
- Investigating problem-solving strategies in programming.
- Identifying common patterns and mistakes among students at different skill levels.
- Designing and evaluating educational interventions to improve programming pedagogy.

### Appendix: Exercise Descriptions <a id="exercise-descriptions"></a>

#### Exercise: Create a To-Do List Webpage <a id="todo"></a>
In this exercise, you will create a simple to-do list webpage using HTML, CSS, and JavaScript. You will work on three files: `index.html`, `script.js`, and `styles.css`. Follow the instructions below to build and style the webpage.

##### HTML Structure
- **Title**: Add a title `<h1>` at the top of your webpage with the text `"Todo List"` and ID `#pageTitle`. Set the font size to `25px` and make the text `bold`.
- **Input Section**:
  - Create an input box `<input type=“text”>` where users can type their tasks. Give this input box the ID `input`.
  - Add a button next to the input box with the text `"Add"` and the ID `#addBtn`.
  - Place the input box and the button inside a `<div>` element with the ID `#inputContainer`.
  - Make sure the input box and the button are aligned horizontally in the same row and centered within this `<div>`.
- **Todo List Container**: Create an empty `<div>` container below the input section where the tasks will appear. Give this container the ID `#todoList`.

##### Add Button Interactivity
- **Adding Items**: When the Add button is clicked, a new task should be added to the `#todoList` container. Each new task should have the class name `.todoItem`. Refer to “Adding and Removing Classes” in the Cheat Sheet for syntax guidance.
- **Task Structure**: Each `.todoItem` should include two elements with class names `.itemContent` and `.deleteBtn`:
  - `.itemContent`: The text of the task from `<input>`.
  - `.deleteBtn`: A button with the text `"Delete"`.
- **Styling the Items**: Set the width of each `.todoItem` to `350px`. Ensure that `.itemContent` and `.deleteBtn` are aligned in the same row, with space between the text and the Delete button.

##### Delete Button Interactivity
- **Deleting Tasks**: When the Delete button is clicked, the entire `.todoItem` should be removed from the list.
- **Styling the Delete Button**:
  - Set the background color of the Delete button to `red`.
  - When you hover over the Delete button, the background color should change to `darkred`.

Follow these requirements to create your to-do list page, making sure your webpage works as described.

#### Exercise: Create an Image Carousel <a id="image"></a>
In this exercise, you will create a simple image carousel webpage using HTML, CSS, and JavaScript. You will work on three files: `index.html`, `script.js`, and `styles.css`. Follow the instructions below to build and style the webpage.

##### HTML Structure
- **Title**: Add a title `<h1>` at the top of your webpage with the text `"Gallery"` and the ID `#pageTitle`. Set the font size to `25px` and make the text `bold`.
- **Thumbnails Section**: Create a `<div>` container below the title for the thumbnails. Give this container the ID `#thumbnails`. This container will eventually display a series of images.
- **Featured Image Section**:
  - Below the thumbnails section, add a `<div>` container with the ID `#featured_container`.
  - Add an `<img>` element with the ID `#featured` in the `#featured_container`. This image will display a larger version of the selected thumbnail.
  - Also, include a `<div>` below the `<img>` element with the ID `#current_description` in the `#featured_container` to show the description of the currently selected image.

##### Thumbnails Generation
- **Images Gallery**:
  - We have provided an array called `images` in your `script.js` starter file. Each element in this array should be an object containing three properties: `url`, `alt`, `id`, and `description`.
  - Write a script that loops through the `images` array and creates a new `<img>` element for each image.
  - Each `<img>` element should be appended to the thumbnails container and should have:
    - Its `src` attribute set to the `url` from `images`.
    - Its `alt` attribute set to the `alt` from `images`.
    - Its `id` attribute set to the `id` from `images`.

- **Styling the Thumbnails**:
  - Ensure all thumbnail images are displayed in a horizontal row and centered in the thumbnails container.
  - Each thumbnail image should have a width of `100px`.

##### Making Images Clickable
- **Click an Image**:
  - Add interactivity so that when a user clicks on a thumbnail, the `src` and `alt` attributes of the `#featured` element are updated to show the selected image.
  - Also, update the `#current_description` element to display the description from `images` associated with the clicked image.

- **Highlight the Selected Image**:
  - Ensure that the currently selected thumbnail image is highlighted with a `1px solid red` border.
  - Make sure that only one image is highlighted at a time. When a new thumbnail is clicked, remove the highlighted class from any previously highlighted image.

- **Styling the Featured Image**:
  - The featured image should be centered and have a width of `500px`.

Follow these requirements to create your image carousel page, ensuring your webpage works as described.

### Contact
For any questions or issues regarding the dataset, please contact [inon@umich.edu].
