<h1>Movie Review Sentiment Analysis and Prediction</h1>
<p>This project was part of my Big Data Analytics course, where we performed end-to-end data analysis, pre-processing, sentiment analysis, and predictive modeling using a movie dataset from data.world and reviews fetched from IMDb.</p>

<h2>Project Overview</h2>
<p>In this project, we selected a primary dataset with movie information from data.world. We enhanced this dataset by fetching reviews from IMDb using the Cinemagoer API, creating a secondary dataset with additional sentiment-related information. The primary goal was to predict movie review sentiments and review scores using various machine learning models.</p>

<h2>Datasets</h2>

<h3>Primary Dataset: Movie Information</h3>
<ul>
    <li><strong>Source:</strong> data.world (<a href="https://data.world/iliketurtles/movie-dataset">https://data.world/iliketurtles/movie-dataset</a>)</li>
    <li><strong>Size:</strong> 3,940 movies</li>
    <li><strong>Contents:</strong> Movie title, Year of Release, Full Summary, Genres, Rating, etc.</li>
</ul>

<h3>Secondary Dataset: IMDb Reviews</h3>
<ul>
    <li><strong>Source:</strong> Fetched using IMDb’s Cinemagoer API</li>
    <li><strong>Size:</strong> 84,135 reviews</li>
    <li><strong>Contents:</strong> Movie IDs, review content, review ratings</li>
</ul>

<h2>Data Collection and Pre-processing</h2>
<ul>
    <li><strong>Challenges:</strong> IMDb API limitations for bulk data retrieval.</li>
    <li><strong>Techniques Used:</strong>
        <ul>
            <li>Batch Processing, Parallel Thread Processing, and Rate Limiting to handle large volumes of data and optimize retrieval.</li>
        </ul>
    </li>
    <li><strong>Data Standardization:</strong> Converted the fetched reviews into a Pandas DataFrame and standardized the data for consistency.</li>
    <li><strong>Text Processing:</strong>
        <ul>
            <li>Language Detection and Filtering</li>
            <li>Text Pre-processing: Tokenization, Stopwords Removal, Lemmatization using NLTK</li>
            <li>Feature Extraction: TF-IDF for numerical representation of text data.</li>
        </ul>
    </li>
</ul>

<h2>Sentiment Analysis</h2>

<h3>Sentiment Scoring</h3>
<ul>
    <li><strong>Tools Used:</strong> SentimentIntensityAnalyzer from NLTK</li>
    <li><strong>Classification:</strong> Reviews classified as positive or negative based on sentiment scores with binary labels created for further exploration.</li>
</ul>

<h3>Data Encoding</h3>
<ul>
    <li><strong>Review Scores:</strong> Encoded as above or below a score of 5.</li>
    <li><strong>Sentiment Labels:</strong> Encoded into binary values for machine learning.</li>
</ul>

<h2>Predictive Modeling</h2>

<h3>Logistic Regression Model</h3>
<ul>
    <li><strong>Target Variables:</strong>
        <ul>
            <li><strong>Sentiment Prediction:</strong> Predict if a future review will be positive or negative.</li>
            <li><strong>Review Score Prediction:</strong> Predict if a review score will be above or below 5.</li>
        </ul>
    </li>
    <li><strong>Approach:</strong> Trained using TF-IDF features from review content.</li>
</ul>

<h3>Additional Models</h3>
<ul>
    <li><strong>Gaussian Naive Bayes (GaussianNB)</strong></li>
    <li><strong>Multinomial Naive Bayes (MultinomialNB)</strong></li>
    <li><strong>Bernoulli Naive Bayes (BernoulliNB)</strong></li>
    <li><strong>Goal:</strong> Compare model performance across different target variables.</li>
</ul>

<h2>Results and Insights</h2>
<ul>
    <li><strong>Model Performance:</strong> Logistic Regression provided robust predictions, with notable differences in performance across sentiment prediction and score prediction tasks.</li>
    <li><strong>Naive Bayes Variants:</strong> Each Naive Bayes variant showed unique strengths depending on the target variable and data distribution.</li>
</ul>

<h2>Technologies Used</h2>
<ul>
    <li><strong>Python:</strong> Primary programming language.</li>
    <li><strong>Pandas:</strong> Data manipulation and cleaning.</li>
    <li><strong>NLTK:</strong> Text pre-processing and sentiment analysis.</li>
    <li><strong>Scikit-Learn:</strong> Machine learning models and TF-IDF Vectorization.</li>
    <li><strong>IMDb Cinemagoer API:</strong> Data collection.</li>
    <li><strong>Parallel Processing:</strong> Optimized API data retrieval.</li>
</ul>

<h2>Key Learnings</h2>
<ul>
    <li><strong>API Management:</strong> Gained experience in handling API limitations and optimizing data collection.</li>
    <li><strong>Text Processing:</strong> Developed a deeper understanding of NLP techniques for sentiment analysis.</li>
    <li><strong>Model Comparison:</strong> Learned the importance of choosing the right model based on the target variable.</li>
</ul>

<h2>Contact</h2>
<p>Feel free to reach out if you have any questions or would like to connect:</p>
<p>Email: <a href="mailto:brandaovh@gmail.com">brandaovh@gmail.com</a><br>LinkedIn: <a target="_blank" rel="noopener noreferrer" href="https://www.linkedin.com/in/brandaovh/">linkedin.com/in/brandaovh/</a></p>
