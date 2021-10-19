# Keyword Aware Influential Community Search in Large Attributed Graphs

<h3>Datasets</h3>

We use three large real datasets: OAG (Open Academic Graph), Twitter and Gowalla that reflect the real life application scenarios to evaluate our proposed algorithms for keyword-aware influential community search.

**OAG** is generated by linking two large academic graphs: Microsoft Academic Graph (MAG) and AMiner. Here, we represent each author as a vertex and co-authorships between authors as edges. This dataset contains more than 150 million academic articles with metadata like title, abstract, authors, keywords provided by authors, etc. We first choose 1, 000 most frequent author-provided keywords as the set of keywords for the attributed graph. Each vertex of the graph is augmented with the semantically relevant set of keywords for the author provided keywords. The score is modeled as the author’s percentile rank (scaled to 1.0), considering the number of citations in publications relevant to a keyword. We skipped non-English articles and the articles with no citation. Finally, there were 10, 714, 737 articles in our dataset. In the attributed graph, we considered the first 1 million authors as vertices and 15,677,940 co-authorship relations among the authors as edges.

**Twitter** dataset is a social network graph of 140,371 users with 2,283,875 follow relations among the users. This dataset also contains the tweets published by these users. Due to Twitter’s privacy policy, any dataset revealing both the users and their tweets can not be shared publicly. However, we share the processed attributed graph where the users are given untraceable identifiers. We process each tweet to filter out tags, website links, and very short words (1-3 characters). Then, we apply tokenization that converts each tweet into a set of token streams. We apply lemmatization on each token to find the root word, and it’s parts-of-speech. Finally, we carefully parse the nouns which are used as keywords in our dataset. We only consider the most frequent 10, 000 keywords for building the attributed graph. The impact of each tweet is evaluated by the number of retweets. We calculate the total number of retweets a user gets from all the tweets associated with a single keyword. In this way, we can assess how popular the user is in Twitter if we consider only that single keyword. We use the percentile of a user’s popularity in a certain keyword (topic) to model his/her influence in that keyword. For example, if a user gets more retweets from “music” related tweets than 98% other users, the user’s influence in “music” keyword is modeled as 0.98.

In **Gowalla** dataset, users are modeled as vertices, and the location ids are considered as keywords. Edges represent the friendship between two users. Each user is augmented with the locations where she checked in. The influence score of a user at a location is modeled as the user’s percentile rank considering the number of check-ins posted by the user at that location. There are 407,533 vertices, 2, 209, 169 edges, and 2, 727, 464 keywords in this attributed graph.

<h3>Links to Raw Dataset</h3>
If you use the raw datasets, please cite appropriate sources.
<ul>
  <li>
    OAG: https://aminer.org/open-academic-graph
  </li>
  
  <li>
    Twitter: Raw dataset cannot be shared publicly due to Twitter’s privacy policy. Please contact the authors if needed.
  </li>
  
  <li>
    Gowalla: http://www.yongliu.org/datasets/index.html
  </li>
</ul>

<h3>Links to Attributed Graph</h3>
Please cite our paper if you use any of the following attributed graphs.

<ul>
    <li>
      OAG: https://drive.google.com/file/d/1ajEFzWMjQZAukMHv8aJ8UAN7otvEW7lp/view?usp=sharing
    </li>
    
    <li>
      Twitter: https://drive.google.com/file/d/1XTCubozlB2TTHkdruW7Na7iyFdS7-GVP/view?usp=sharing
    </li>
  
    <li>
      Gowalla: https://drive.google.com/file/d/16PsulYlA9wCjjDphTpslq8Yqgz51b5Lo/view?usp=sharing
    </li>
  
</ul>
Attributed graphs are publicly available at https://drive.google.com/drive/folders/1yU32kH6E2xvQow8hxCbCtMoFASDVn4TE?usp=sharing.
