<h1>Movie Review Sentiment Analysis and Prediction</h1>
<p>This project involved analyzing a combined dataset extracted from a CSV file on data.world and reviews obtained from IMDb through an API. We conducted end-to-end data analysis, pre-processing, sentiment analysis, and predictive modeling.</p>

<h2>Project Overview</h2>
<p>In this project, we selected a primary dataset with movie information from data.world. From there, we extracted a list of movie IDs to fetch review data from IMDb through the Cinemagoer API, creating a secondary dataset with additional sentiment-related information. The primary goal was to predict movie review sentiments and review scores using various machine learning models.</p>

<h2>Technologies Used</h2>
<ul>
    <li><strong>Python:</strong> Primary programming language.</li>
    <li><strong>Pandas:</strong> Data manipulation and cleaning.</li>
    <li><strong>NLTK:</strong> Text pre-processing and sentiment analysis.</li>
    <li><strong>Scikit-Learn:</strong> Machine learning models and TF-IDF Vectorization.</li>
    <li><strong>IMDb Cinemagoer API:</strong> Data collection.</li>
</ul>

<h2>Datasets</h2>

<h3>Primary Dataset: Movie Information</h3>
<ul>
    <li><strong>Source:</strong> data.world (<a href="https://data.world/iliketurtles/movie-dataset">https://data.world/iliketurtles/movie-dataset</a>)</li>
    <li><strong>Size:</strong> 3,940 movies</li>
    <li><strong>Contents:</strong>
        Movie title, Year of Release, Full Summary, Genres, Rating, etc.
    </li>
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
    <li><strong>Techniques Used:</strong> Batch Processing, Parallel Thread Processing, and Request Throttling to handle large volumes of data and optimize retrieval.</li>
    <li><strong>Data Standardization:</strong> Converted the fetched reviews into a Pandas DataFrame and standardized the data for consistency.</li>
    <li><strong>Text Processing:</strong>
        <ul>
            <li>Language Detection and Filtering</li>
            <li>Text Pre-processing: Tokenization, Stopwords Removal, Lemmatization using NLTK</li>
            <li>Feature Extraction: TF-IDF for numerical representation of text data.</li>
        </ul>
    </li>
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
</ul>

<h3>Additional Models</h3>
<ul>
    <li><strong>Gaussian Naive Bayes (GaussianNB)</strong></li>
    <li><strong>Multinomial Naive Bayes (MultinomialNB)</strong></li>
    <li><strong>Bernoulli Naive Bayes (BernoulliNB)</strong></li>
</ul>

<h2>Results and Insights</h2>
<li><strong>Model Performance:</strong> The Logistic Regression model achieved an accuracy of 91% in predicting sentiment labels and 89% in predicting review scores, as measured by the weighted average F1-score. However, the model exhibited a tendency to overestimate positive sentiment and high review scores, likely due to the imbalanced dataset with a 4:1 ratio of positive/high-score to negative/low-score reviews. Considering this, it is important to have caution and consider the recall scores when using this model to evaluate new data.</li>
<li><strong>Naive Bayes Variants:</strong> All models underperformed compared to Logistic Regression, as anticipated. This result aligns with the understanding that Logistic Regression can better capture complex relationships between features (in this case, words) compared to Naive Bayes models, which operate under the assumption of feature independence. Given the importance of word dependencies in sentiment and score prediction, this outcome is consistent with expectations.</li>
</ul>

<h2>Key Learnings</h2>
<ul>
    <li><strong>API Management:</strong> Gained experience in handling API limitations and optimizing data collection.</li>
    <li><strong>Text Processing:</strong> Developed a deeper understanding of NLP transformation and pre-processing techniques for sentiment analysis.</li>
    <li><strong>Model Comparison:</strong> Learned the importance of choosing the right ML model based on trained features and targets.</li>
</ul>

<h2>Contact</h2>
<p>Feel free to reach out if you have any questions or would like to connect:</p>
<p>Email: <a href="mailto:brandaovh@gmail.com">brandaovh@gmail.com</a><br>LinkedIn: <a target="_blank" rel="noopener noreferrer" href="https://www.linkedin.com/in/brandaovh/">linkedin.com/in/brandaovh/</a></p>
