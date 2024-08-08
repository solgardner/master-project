Upon recieving this dataset, I first had to clean up the data. This was fairly easy, as most data was already numerical, with the exception of the actuall subreddits. Changing this and deleting a few columns that I deemed unnessicary for this project, all I wanted was the lexicon data, and it was ready to be used in a neural network. I ran three nerual networks to find the best loss values.

All three networks contained two hidden layers and relu activation functions, having different node counts in their second layer. The first neural network contained one hidden layer with fourty eight nodes, and a subsequent layer also containing fourty eight nodes. This resulted in a sharp decline in the Mean Absolute Error, flattening to a final loss value of roughly 1.3. The seconed neural network doubled the second hidden layer to ninty six nodes. This gave a smoother curve, resulting in a final loss value of 0.34. Finally, decreasing the second hidden layer neuron count to twenty four yielded a Mean Absolute Error graph between the two preceeding networks, and finished with a loss of 0.36. In conclusion, increasing the second layers neuron count resulted in a more accurate end loss value, although supprisingly, decreasing it gave a very similar result.


  For the next two means of analysis, I needed correlation. The more correlated my two axis were, the more interesting and valuable the results. To do this, I used the pandas builtin corrilation function. Unfortunatly, this did not return any great results (Close to |1|), but I made do with two values, *social_upvote_score* and *subreddit.* These had a correlation value of roughly 0.2.

  Firstly, I built the K-Means Clustering algorithim, which groups data into K different Clusters. First, it chooses K random points, than moves them iterativly into the best possible locations. This returned less than ideal values, as the data wasn't great, but the best data is shown in [KMeans.png](https://).


Finally, I built the K-Nearest Neighbors algorithim. This algorithm takes a data point and compares it to the K nearest neigbors, catagorizing with whatever has the majority. Again, this was not an ideal value, with an accuracy score of 0.27692307692307694

In conclusion, while this project showed less than ideal results, it taught me how to take any dataset and analyze it from start to finish. Previously, all I had done was small parts of this larger process, and taking on the project in it's entierety was a bit daunting. However, I found that approaching it one step at a time made it manageble. 
