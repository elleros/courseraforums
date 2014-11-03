# Description of the CSV files

### course_information.csv
* __name__ course name
* __course_id__ Coursera course identifier
* __weeks__ course duration (in weeks)
* __hours__ average number of hours requested per week
* __start_date__ start date
* __end_date__ end date (often not enetered in this file)
* __type__ type of course ('Q': quantitative, ...)
* __language__
* __num_threads__ number of threads in the forum
* __mandatory_posts__ 
* __num_users__ number of users

### course_subforums.csv
* __thread_id__
* __course_id__ Coursera course identifier
* __og_forum__
* __og_forum_id__
* __parent_forum__
* __parent_forum_id__
* __forum_chain__
* __depth__
* __num_views__ number of views
* __num_tags__ number of tags associated to the subforum title
* __forum_id__

### course_posts.csv
* __post_id__
* __thread_id__
* __course_id__ Coursera course identifier
* __parent_id__
* __order__
* __user_id__ user ID (hashed version of original Coursera ID)
* __user_type__
* __post_time__
* __relative_t__
* __votes__
* __forum_id__


This repository is associated to the paper:
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
