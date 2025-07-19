# 🏏 IPL Win Predictor with Dynamic Background 🏆

Predict the outcome of IPL matches using real-time conditions and a trained machine learning model! This project estimates the win probability of teams based on current match dynamics. Experience the excitement with a dynamic background that reflects the game's intensity! 🤩<br>
<br>
**Link to the Like Site: https://rapogi2456.pythonanywhere.com/**

[![License](https://img.shields.io/badge/License-MIT%20%7C%20GPL%20%7C%20AFL-yellow.svg)](LICENSE)

## Table of Contents

- [Project Overview](#project-overview)
- [Directory Structure](#directory-structure)
- [Data Sources](#data-sources)
- [Website Preview](#website-preview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Setup and Installation](#setup-and-installation)
  - [Prerequisites](#prerequisites)
  - [Backend Setup](#backend-setup)
  - [Frontend Setup](#frontend-setup)
- [Usuage](#usuage)
- [Machine Learning Model](#machine-learning-model)
- [Future Enhancements](#future-enhancements)
- [Contribution](#contribution)
- [License](#license)
- [Contact](#contact)

## Project Overview💡

This project uses machine learning to predict the win probability of teams in an Indian Premier League (IPL) match. By analyzing real-time conditions such as the current score, wickets fallen, and overs remaining, the model provides the percentage chance of each team winning. This allows fans to get a data-driven perspective on the match's progress! 📈

## Directory Structure📁
<pre>
Directory structure:
└── daxgupta-ipl_win_predictor_with_slideshow_background/
    ├── README.md
    ├── app1.py
    ├── pipe.pkl
    ├── static/
    │   ├── css/
    │   │   └── style.css
    │   └── js/
    │       └── script.js
    └── templates/
        └── index.html
</pre>

## Data Sources🗄

The data for this project was sourced from:

*   **Official IPL Website:** Used for basic match information and results.
*   **Cricinfo API:**  Accessed for detailed ball-by-ball data, player statistics, and match commentary.  A custom script was developed to extract and format the data.

Data was collected using web scraping techniques and the Cricinfo API. The collected data was then cleaned and preprocessed using Pandas in Python to handle missing values, correct data types, and ensure consistency. Data validation included cross-referencing information between the IPL website and Cricinfo to ensure accuracy.

## Website Preview🌐
![ipl-win-pred](https://github.com/user-attachments/assets/2acd2c9b-47f7-4bae-98ad-6a70dc86c62d)

## Features✨
* **Predictive Analysis:** Predicts the winning probability for both batting and bowling teams based on real-time match data.
* **User-Friendly Interface:** An intuitive web form to input match details.
* **Dynamic Background:** A beautiful slideshow of IPL-related images in the background, enhancing the visual appeal.
* **Responsive Design:** Optimized for various screen sizes (desktop, tablet, mobile) using Tailwind CSS.
* **Client-side Validation:** Ensures valid input before sending data to the backend.
* **Error Handling:** Provides clear messages for validation errors and backend issues.
> **Note:** Elaborate on how the dynamic background changes based on specific match events (e.g., background turns red when a wicket falls, changes to team colors based on the current leading team). Include any relevant configuration options for customizing the background behavior.  For example, mention any configuration files or settings where users can customize the color schemes or trigger events.

## Technologies Used🧑‍💻
* **Backend:**
    * ***Python 3.x***
    * ***Flask:*** Web framework for the API.
    * ***Pandas:*** Data manipulation.
    * ***Scikit-learn (implied by pipe.pkl):*** For the machine learning model.
    * ***pickle:*** To load the pre-trained ML model.
    * ***Flask-CORS:*** For handling Cross-Origin Resource Sharing.

* **Frontend:**
    * ***HTML5***
    * ***CSS3 (with custom styles and Tailwind CSS)***
    * ***JavaScript (ES6+)***

  <br>
  
## Setup and Installation🛠

Follow these steps to get the project up and running on your local machine.

### Prerequisites
 * Python 3.x installed.
 * pip (Python package installer).
    
### Backend Setup
1. ***Clone the repository:***
    <pre> git clone &lt;repository_url&gt;
    cd daxgupta-ipl_win_predictor_with_slideshow_background</pre>
    (Replace `<repository_url>` with the actual URL of your Git repository if applicable.)
    
2. ***Create a virtual environment (recommended):***
    <pre> python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate</pre>

3. ***Install backend dependencies:***
    <pre>pip install Flask Flask-Cors numpy pandas scikit-learn</pre>
    
4. ***Ensure the model file is present:*** <br>
    Make sure `pipe.pkl` is in the root directory of your project, alongside app1.py. This file contains the pre-trained machine learning model.

5. ***Run the Flask backend:***
    <pre> python app1.py</pre>
    
    The backend server will typically run on `http://127.0.0.1:5000`. You should see output in your terminal indicating that the model has loaded and the Flask app is running.

### Frontend Setup
1. ***Navigate to the project root:*** <br>
    Ensure you are in the `daxgupta-ipl_win_predictor_with_slideshow_background/` directory.

2. ***Open `index.html`:*** <br>
    Simply open the `templates/index.html` file in your web browser. The JavaScript will handle the dynamic background and form interactions, communicating with the Flask backend. <br>
    
    Note: The `script.js` file expects image paths to be relative to the `static/images/` directory. If you move index.html or the `static` folder, you might need to adjust these paths.

## Usuage🚀
1. **Start the Backend:** Run `app1.py` as described in the Backend Setup section.
2. **Open the Frontend:** Open `templates/index.html` in your web browser.
3. **Input Match Details:**
    * Select the Batting Team and Bowling Team.
    * Select the Venue City.
    * Enter the Target Score set by the first innings.
    * Enter the Current Score of the batting team.
    * Enter the number of Wickets Down.
    * Enter the Overs Completed (e.g., `12.5 for 12 overs and 5 balls`).
4. **Get Prediction:** Click the `"Predict Winning Probability"` button.
5. **View Results:** The application will display the predicted winning probabilities for both teams. Error messages will appear if any input is invalid or if there's a problem connecting to the backend.

## Machine Learning Model🤖
The core of the prediction logic resides in `pipe.pkl`, which is a pre-trained machine learning model (likely a Logistic Regression model within a scikit-learn pipeline, as suggested by the `pipe.pkl` content). The `app1.py` script loads this model and performs feature engineering (calculating runs left, balls left, current run rate, required run rate) before making predictions.

## Future Enhancements🔬

-   [ ] Implement real-time data updates using APIs for live match data. 📡
-   [ ] Improve the accuracy of the prediction model by incorporating more features and advanced algorithms. 🧠
-   [ ] Add more visualization options, such as historical win probability graphs. 📈
-   [ ] Deploy to a cloud platform (e.g., Heroku, AWS) for broader accessibility. ☁️
-   [ ] Implement user authentication and personalized match predictions. 👤

> **Note:** Include a detailed roadmap of planned features and improvements. Prioritize the enhancements and provide estimated timelines, if possible. Consider adding a section for known issues and limitations.

## Contribution🤝

Contributions are welcome and encouraged! 🎉 Please follow these steps:

1.  Fork the repository. 🍴
2.  Create a new branch for your feature or bug fix: `git checkout -b feature/your-feature-name`. 🌿
3.  Make your changes and ensure they adhere to the project's coding standards. 💻
4.  Commit your changes with descriptive commit messages: `git commit -am 'Add descriptive message'`. ✍️
5.  Push to your branch: `git push origin feature/your-feature-name`. 🚀
6.  Create a new Pull Request. 📤

> **Note:** Add specific guidelines for contributing, such as coding standards (e.g., PEP 8 for Python), testing procedures, and documentation requirements. Specify where to report bugs or suggest new features. For example, link to the issues page.

## License📝

This project is licensed under the MIT, GPL, and AFL licenses. See the `LICENSE` file for more details. 📜

## Contact📞
