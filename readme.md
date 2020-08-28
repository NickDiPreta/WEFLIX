## Project Links
- [Live Link](https://stark-plateau-00385.herokuapp.com/) (guest log in is username: guest@hotmail.com password: guestpassword )
- [Medium Article about The Recommender Engine](https://medium.com/@nicholasdipreta2020/how-to-create-a-user-user-collaborative-filtering-recommender-system-in-ruby-rails-react-js-36f89b4dce05)
## **Project Overview:**

*WeFlix is an app designed to help groups of people settle on a movie to watch together. A user can add friends of theirs to a group. Once everyone has been added to the group, WeFlix will choose a few movies for them to watch!*


### **Background Knowledge**
**Collaborative Filtering**:

Some recommender engines are powered by collaborative filtering systems where recommendations are generated based on how other users respond to the same items. Let’s say that we wanted to recommend a movie to our friend Tanya. Tanya and I had seen the same movies and liked them all, except I had seen Avatar and she hadn’t. If I liked Avatar, it would make sense that Tanya would like Avatar as well since we have similar preferences, so a collaborative filtering recommendation engine would recommend that movie to her. I decided to utilize this method because the only data I wanted to have in my database was users and movies that each user liked. 

**Jaccard Index: The Algorithm Powering the Engine**
I knew I wanted to go with a User-User collaborative filtering recommender system, I needed to find an algorithm that would allow me to find nearest neighbors to each user. I found the simple and beautiful Jaccard Index would suit my purposes perfectly.The measurement emphasizes similarity between finite sample sets, and is formally defined as the size of the intersection divided by the size of the union of the sample sets. The higher the index, the more similar our sets were.
![jaccardindex](https://miro.medium.com/max/700/0*WUA18DFvGiV8p5Q1)

**Dataset Limitations** :

I initially used a dataset with nearly 100,000 rows. Generating a recommendation based on this dataset took almost 3 minutes for a single user! By reducing my dataset to 60 users with 5 movie preferences each, I reduced the recommendation time from almost 2 minutes down to around 50ms. This 3600X increase came at the cost of accuracy but was essential to getting the recommender system operational by the project deadline.

**Conclusion**

While I set out to learn how to build a recommender system, I also learned, how to boil down a real-world problem for a product to a form so simple that computer logic could make sense of it, how to research algorithms and analyze their practicality in a specific use context, and balance optimization/time complexity with the accuracy of my results due to limited computing and storage capacity. 


### Models
![models](https://i.imgur.com/UTo4485.png)


### 3rd Party APIS
- TMDB API used to get cover art and movie years.

### Additional Dependencies 
1. Styled-components
2. React Router
3. React-Transition-Group
4. B-crypt (gem)
5. cors (gem)