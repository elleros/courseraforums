# file_information


## course_information.csv
* name: course name
* course_id: Coursera course identifier
* weeks: course duration (in weeks)
* hours: average number of hours requested per week
* start_date: start date
* end_date: end date (often not enetered in this file)
* type: type of course ('Q': quantitative, ...)
* language: 
* num_threads
* mandatory_posts
* num_users

## course_subforums.csv
* thread_id
* course_id
* og_forum
* og_forum_id
* parent_forum
* parent_forum_id
* forum_chain
* depth
* num_views
* num_tags
* forum_id

## course_posts.csv
* post_id
* thread_id
* course_id
* parent_id
* order
* user_id
* user_type
* post_time
* relative_t
* votes
* forum_id



[Language independent analysis and classification of discussion threads in coursera MOOC forums](http://www2.cs.uh.edu/~gnawali/papers/coursera-iri2014-abstract.html), by Lorenzo A. Rossi and Omprakash Gnawali, IEEE International Conference on Information Reuse and Integration (IRI), August 2014.

The dataset has been anonymized as follows: the text and the names of the authors of all the posts and comments have been removed. The author indentifiers have been re-encoded so not to much the Coursera indentifiers.

If you use the dataset for your work, please cite the paper. __BiBTeX entry:__

@inproceedings{coursera-iri2014,
   author = {Lorenzo A. Rossi and Omprakash Gnawali},
   title = {{Language Independent Analysis and Classification of Discussion Threads in Coursera MOOC Forums}},
   booktitle = {Proceedings of the IEEE International Conference on Information Reuse and Integration (IRI 2014)},
   month = aug,
   year = {2014}
}