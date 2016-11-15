# courseraforums
This repository provides the anonymized versions of the discussion threads from the forums of 60 Coursera Massive Open Online Courses (MOOCs), for a total of about 100,000 threads. This dataset is associated to the paper:
[Language independent analysis and classification of discussion threads in coursera MOOC forums](http://www2.cs.uh.edu/~gnawali/papers/coursera-iri2014-abstract.html), by Lorenzo A. Rossi and Omprakash Gnawali, IEEE International Conference on Information Reuse and Integration (IRI), August 2014.

If you use the dataset for your work, please cite the paper. __BiBTeX entry:__
```
@inproceedings{coursera-iri2014,
   author = {Lorenzo A. Rossi and Omprakash Gnawali},
   title = {{Language Independent Analysis and Classification of Discussion Threads in Coursera MOOC Forums}},
   booktitle = {Proceedings of the IEEE International Conference on Information Reuse and Integration (IRI 2014)},
   month = aug,
   year = {2014}
}
```
If you have questions, email lorenzo __[dot]__ rossi __[at]__ gmail

The dataset has been anonymized as follows: the text and the names of the authors of all the posts and comments have been removed. The author indentifiers have been hashed so not to match the Coursera user indentifiers. Anonymous users have ID 0 on this repository as well as on Coursera.

## Description of the CSV files

### course_information.csv
Basic information about the 60 courses used in this dataset.
* __name__ course name
* __course_id__ Coursera course identifier
* __weeks__ course duration (in weeks)
* __hours__ average number of hours ofcourse work requested per week
* __start_date__ start date
* __end_date__ end date (often not enetered in this file)
* __type__ type of course ('Q': quantitative, ...)
* __language__ language use to teach the course (also the main but not necessarily the only language of the forums). 'E': English, 'FR': French, 'SP': Spanish, 'CH': Chinese  
* __num_threads__ number of threads in the forum
* __mandatory_posts__ number of posts to receive credits for activity in the forums some Coursera courses give credits for posting in the forums 
* __num_users__ number of unique users active in the forum. Anonymous users are counted as 1 unit; so the number of actual users may be larger.

### course_subforums.csv
Data about the threads and the subpforums containing them for the discussion forums of the 60 courses.
* __thread_id__ thread identifier
* __course_id__ Coursera course identifier
* __og_forum__  name of the original (sub)forum
* __og_forum_id__ identifier (int) of the original subforum
* __parent_forum__ name of the parent (sub)forum
* __parent_forum_id__ identifier of the parent (sub)forum
* __forum_chain__ complete sequence of (sub)forum names from root to current subforum
* __depth__ number of (sub)forum in forum_chain
* __num_views__ number of views for the thread
* __num_tags__ number of tags associated to the subforum title
* __forum_id__ possibly re-mapped subforum identifier 
   * 2: General (Miscellaneous) Discussion
   * 3: Assignments 
   * 4: Study Groups / Meetups
   * 7: Course Feedback / Suggestions
   * 8: Lectures
   * 9: Platform Issues
   * 100: Signature Track
   * otherwise: not remapped 

### course_posts.csv
Data aboout all the posts or comments (minus spam) made in the discussion forums of the 60 courses.
* __post_id__ identifier (integer) of the post (comment) 
* __thread_id__ identifier of the thread
* __course_id__ Coursera course identifier
* __parent_id__ identifier of the parent post (0 for posts, nonzero for comments) 
* __order__ order of the post in the thread (1: first post, 2: ..., 0: comment)
* __user_id__ user ID (hashed version of original Coursera user ID)
* __user_type__  'Student', 'Anonymous', 'Staff', 'Instructor', 'Community TA', 'Coursera Staff' or 'Coursera Tech Support'
* __post_time__ time stamp
* __relative_t__ normalized posting time relative to the course's start and end time
* __votes__ sum of the votes received by the post (comment). Each user can add +/-1 to a post
* __num_words__ (**new**) number of words (NA for posts in Chinese language)
* __forum_id__ possibly re-mapped subforum identifier 
   * 2: General (Miscellaneous) Discussion
   * 3: Assignments 
   * 4: Study Groups / Meetups
   * 7: Course Feedback / Suggestions
   * 8: Lectures
   * 9: Platform Issues
   * 100: Signature Track
   * otherwise: not remapped 
