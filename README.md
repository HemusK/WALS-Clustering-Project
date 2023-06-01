# WALS-Clustering-Project
This is a pretty straightforward project where I grabbed some data from the World Atlas of Language Structures and processed it to try and elucidate if groupings based on linguistics features could approximate a language family.
Using pandas I manipulated the spreadsheet into a format that would be proper for the machine learning model and then used dimensionality reduction to map to two dimensions. This is so that I could easily visualize the similarities, and apply clustering methods to them as many do not work well with larger datasets. I did not go with a clustering method like k-means as I was not entirely sure how many groups would be necessary. I also did not want them to be of equal size. Real language families are not of equal size, with some families like Indo-European, Niger-Congo and Afro-Asiatic covering thousands of languages over a large area, while others like Dravidian, Koreanic and Japonic being relegated to a single region and having few closely related languages.

# Conclusions
Ultimately, I found that the language data did not closely correspond with any areal or genealogical groupings, as can be shown in the final map. However, many sign languages clearly clustered together very well unlike many of the spoken languages.
One flaw of this project is that I treated all the data as numerical in order to apply the clustering algorithm onto them and make it easier to visualize. This means that if a language has a value of 5 for a specific feature in the dataset it would be treated as more similar to a language with a value of 6 for the same feature. While this makes sense for some features like the size of consonant inventory, for other features like primary word order where the label is simply a categorical one, it does not. If I do this project again, I will try using a decision tree or other algorithm that can handle categorical as well as numerical data instead to assign the groupings.
