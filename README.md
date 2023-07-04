# Project6-OpenClassrooms
Classify consumer goods
## Business case
The company "Place de marché" wants to launch an e-commerce marketplace. On the marketplace, sellers offer items to buyers by posting a photo and a description. For now, the item’s categorization is done manually by sellers, and is therefore unreliable, and the volume of items is currently very small.
To improve the user experience for sellers (facilitate the posting of new items) and buyers (facilitate the search), and with a view to scaling up, it becomes necessary to automate this task.
## Objectives
Carry out a first feasibility study of a classification engine, based on the products images and descriptions, for the categorization automation.
## Main results
To summarize, I have:

-	tested several approaches for extracting text features. Word embedding approaches outperform Bag-of-Words-like approaches, probably because they better capture relationships between words in a sentence. The best data encoding was obtained with USE; the clustering of the extracted features allows the correct categorization of 2/3 of the products.
-	tested several approaches for extracting image features. Transfer learning outperform SIFT/ORB approaches. The best clustering was achieved by using features extracted with ResNet50, with max pooling. Clustering allows the correct categorization of 55% of products.

Clustering of text features allows to better identify certain categories, while clustering of image features allows to better identify others. The two approaches complement and reinforce each other: by taking the best clustering, text or image, for each category, it is possible to correctly classify the 85% of products, which demonstrate the feasibility of the classification engine. The feasibility was confirmed by a classification test: an SVC trained on all the features, text and image, correctly classified 94.7% of products.

These results could be further improved. Indeed, neither the USE model nor the ResNet were fine-tuned. A fine tuning of the models could better adapt them to the problem of product classification and therefore lead to better accuracy.
## Acquired skills
-	Graphically represent large-scale data
-	Pre-process text data 
-	Preprocess image data 
-	Implement dimension reduction techniques
-	Developing a deep learning model
-	Evaluate the performance of deep learning models 

