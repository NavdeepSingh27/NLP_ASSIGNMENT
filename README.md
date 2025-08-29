Word Embeddings: Context and Visualization 📊
This project helps you understand word embeddings by generating and visualizing them from text. We'll use a count-based approach where a word's meaning is learned from its surrounding words.

What It Does ✨
The script performs the following key tasks:

Identifies unique words in your text.

Builds a "co-occurrence" matrix, counting how often words appear near each other.

Shrinks these word representations using PCA to make them easier to work with.

Plots the words in 2D space, letting you see how related words cluster together.

Getting Started ▶️
To run this project:

Save the Python code: Copy the co_occurrence_embeddings code (from the editor) into a file named co_occurrence_analysis.py.

Install tools: Make sure you have these libraries installed:

pip install numpy matplotlib scikit-learn

Run it: Execute the script from your terminal:

python co_occurrence_analysis.py

You'll see output in your console and a pop-up window showing the 2D word plot!

The Text You'll Use 📚
The script comes with a built-in, diverse collection of sentences. This helps demonstrate how word relationships are captured, preventing all words from clumping too closely in the visualization.

A few examples from the corpus:

"The sun shines brightly in the clear blue sky."

"Cats are playful pets, but dogs are loyal companions."

"Computers process information quickly, enabling new technologies."

How It Works Under the Hood 🛠️
The project is broken down into simple steps:

get_distinct_words(corpus)
This function finds all the unique words in your text. It cleans them up by making everything lowercase and removing punctuation.

construct_co_occurrence_matrix(corpus, window_size=4)
This is where the magic happens! It creates a grid (a matrix) that counts how many times words appear together. The window_size (defaulting to 4, but set to 3 in the example run) determines how many words on either side of a central word are considered its "neighbors."

perform_dimensionality_reduction(matrix, k_dimensions=2)
Since our co-occurrence matrix can be very large, this function uses Principal Component Analysis (PCA) to reduce the number of dimensions to k_dimensions (we use 2 for plotting). Think of it as finding the most important angles to view the data from, making it simpler without losing too much information.

plot_vectors_2d(vectors, word_labels, title="2D Word Embeddings")
Finally, this function takes those 2-dimensional word representations and draws them on a graph. Each word is a point, and its label appears next to it. You'll notice that words used in similar contexts tend to appear closer together, visually representing their semantic connection.

Tools Used 📦
numpy: For handling all the number crunching and matrix operations.

collections (defaultdict): Helps with efficient counting.

matplotlib: Creates those nice 2D plots.

scikit-learn (PCA): Our go-to for dimensionality reduction.

re: For text cleaning and finding words.

Want to Do More? 🚀
Here are some ideas to expand the project:

Smarter text cleaning: Add steps to remove common "stop words" (like "the," "a") or reduce words to their base form (like "running" to "run").

Load bigger texts: Make it read from any large text file you provide.

Try other visualizations: Explore techniques like t-SNE for different ways to see the word relationships.

Test the quality: Add ways to check how good your word embeddings are, perhaps by testing if they can solve word puzzles.
