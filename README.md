<!DOCTYPE html>
<html lang="en">
<head>
</head>
<body>

<h1><i class="fas fa-podcast"></i> Podcast Scraping: Extracting Data from 'Compuesto' Podcast</h1>

<h2><i class="fas fa-info-circle"></i> 📌 Introduction</h2>
<p>This project aims to extract detailed information from the "Compuesto" podcast by Andrés Garza on Spotify using the Spotify API and the Spotipy library.</p>

<h2><i class="fas fa-bullseye"></i>🎯 Objectives</h2>
<ul>
    <li>Obtain podcast data from Spotify.</li>
    <li>Extract key information from each episode (title, description, date, duration, guests, and mentioned companies).</li>
    <li>Save the results in a CSV file for further analysis.</li>
</ul>

<h2><i class="fas fa-microphone"></i>🎙️ About the Podcast</h2>
<ul>
    <li><strong>Name:</strong> Compuesto</li>
    <li><strong>Author:</strong> Andrés Garza</li>
    <li><strong>Description:</strong> COMPUESTOS Podcast is designed to inspire, teach, and communicate ideas and stories from various personalities who overcame challenges to achieve their current state.</li>
    <li><strong>Link:</strong> <a href="https://open.spotify.com/show/3kLgH97biRRk4BheBzysbn" target="_blank">Compuesto Podcast on Spotify</a></li>
</ul>

<h2><i class="fas fa-check-circle"></i> Conclusions</h2>
<p>Based on the objectives set, the following observations were made:</p>
<ul>
    <li><strong>Identification of Guests and Mentioned Companies:</strong> The analysis of podcast description texts successfully identified guests and mentioned companies in each episode. The combination of regular expressions and the Spanish Natural Language Processing (NLP) model (spaCy) proved effective in extracting this information, improving precision and reducing false positives. Specific text patterns, along with the NER model, resulted in considerably more accurate entity extraction. Implementing a function to remove duplicates ensured the quality of the obtained information.</li>
    <li><strong>Precision in Entity Extraction:</strong> Several improvements were made to the algorithm to increase precision. Regular expressions allowed the extraction of crucial information present in specific formats in the descriptions, such as the guest's name before the "Redes del Invitado" section or mentions through the phrase "Hoy está con nosotros." Applying these rules increased the precision of guest detection in episodes. Additionally, mechanisms to avoid common false positives and improve the quality of description processing were implemented. Excluding creator names, verifying false positives like "Invitado" or "Redes," and removing companies that were only acronyms contributed to cleaner and more precise information.</li>
    <li><strong>Processing Efficiency:</strong> The code is designed to optimize dataframe processing, demonstrating real-time progress, which is crucial for large datasets. The estimated time to complete the process is provided to the user, facilitating process tracking and better execution time management.</li>
</ul>

<h2><i class="fas fa-exclamation-triangle"></i> Limitations</h2>
<ul>
    <li>The success of the model depends on the quality and consistency of the text in the podcast descriptions.</li>
    <li>The NLP model used may not be 100% accurate and may have errors in identifying guests or companies.</li>
</ul>

<h2><i class="fas fa-cogs"></i> Future Work</h2>
<ul>
    <li>Evaluate other NLP models or incorporate more advanced techniques to improve precision.</li>
    <li>Explore different methods for information extraction, such as using deep learning models.</li>
    <li>Develop a graphical interface to facilitate the use and visualization of results.</li>
    <li>Expand functionality to include other types of entities (topics, concepts, etc.).</li>
</ul>

</body>
</html>
