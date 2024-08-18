<h1>Movie Review Sentiment Analysis and Prediction</h1>
<p>This project was part of my Big Data Analytics course, where we performed end-to-end data analysis, pre-processing, sentiment analysis, and predictive modeling using a movie dataset from HydraHD and reviews fetched from IMDb.</p>

<h2>Project Overview</h2>
<p>In this project, we selected a primary dataset with movie information from HydraHD. We enhanced this dataset by fetching reviews from IMDb using the Cinemagoer API, creating a secondary dataset with additional sentiment-related information. The primary goal was to predict movie review sentiments and review scores using various machine learning models.</p>

<h2>Datasets</h2>

<h3>Primary Dataset: HydraHD Movie Information</h3>
<ul>
    <li><strong>Source:</strong> HydraHD (Hydra)</li>
    <li><strong>Size:</strong> 4,000+ movies</li>
    <li><strong>Contents:</strong> Movie IDs, titles, genres, release dates, etc.</li>
</ul>

<h3>Secondary Dataset: IMDb Reviews</h3>
<ul>
    <li><strong>Source:</strong> Fetched using IMDb’s Cinemagoer API</li>
    <li><strong>Size:</strong> Matched to the HydraHD dataset</li>
    <li><strong>Contents:</strong> Movie IDs, review content, review ratings</li>
</ul>

<h2>Data Collection and Pre-processing</h2>

<h3>IMDb Review Extraction</h3>
<ul>
    <li><strong>Challenges:</strong> IMDb API limitations for bulk data retrieval.</li>
    <li><strong>Techniques Used:</strong>
        <ul>
            <li><strong>Batch Processing:</strong> To handle large volumes of requests.</li>
            <li><strong>Parallel Thread Processing:</strong> To speed up data retrieval.</li>
            <li><strong>Rate Limiting:</strong> To avoid API rate limits.</li>
        </ul>
    </li>
</ul>

<h3>Data Standardization</h3>
<p>Converted the fetched reviews into a Pandas DataFrame. Standardized the data to ensure consistency across datasets.</p>

<h3>Text Processing</h3>
<ul>
    <li><strong>Language Detection:</strong> Identified and filtered reviews based on language.</li>
    <li><strong>Text Pre-processing:</strong>
        <ul>
            <li>Tokenization</li>
            <li>Stopwords removal</li>
            <li>Lemmatization using NLTK</li>
        </ul>
    </li>
    <li><strong>Feature Extraction:</strong> Used Term Frequency-Inverse Document Frequency (TF-IDF) to transform text data into numerical features.</li>
</ul>

<h2>Sentiment Analysis</h2>

<h3>Sentiment Scoring</h3>
<ul>
    <li><strong>Tools Used:</strong> SentimentIntensityAnalyzer from NLTK</li>
    <li><strong>Classification:</strong> Reviews were classified as positive or negative based on sentiment scores. Binary labels were created for further exploration.</li>
</ul>

<h3>Data Encoding</h3>
<ul>
    <li><strong>Review Scores:</strong> Encoded review scores above or below 5.</li>
    <li><strong>Sentiment Labels:</strong> Encoded sentiment labels into binary values for machine learning.</li>
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

<h2>Repository Structure</h2>
<ul>
    <li><strong>/data:</strong> Contains sample datasets used for modeling.</li>
    <li><strong>/scripts:</strong> Includes Python scripts for data collection, pre-processing, and modeling.</li>
    <li><strong>/notebooks:</strong> Jupyter notebooks demonstrating the end-to-end process.</li>
    <li><strong>/reports:</strong> Documentation and results analysis.</li>
</ul>

<h2>How to Run</h2>
<ol>
    <li>Clone the repository.</li>
    <li>Install the required packages:
        <pre><code>pip install -r requirements.txt</code></pre>
    </li>
    <li>Run the Jupyter notebooks or scripts in the <code>/scripts</code> directory.</li>
</ol>

<h2>Demo</h2>
<p>Check out the demo of the project in this <a href="#">video link</a>.</p>

<h2>Contact</h2>
<p>Feel free to reach out if you have any questions or would like to connect:</p>
<p>Email: <a href="mailto:brandaovh@gmail.com">brandaovh@gmail.com</a><br>LinkedIn: <a target="_blank" rel="noopener noreferrer" href="https://www.linkedin.com/in/brandaovh/">linkedin.com/in/brandaovh/</a></p>
