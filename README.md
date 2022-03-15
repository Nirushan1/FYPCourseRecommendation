# System :mortar_board:

Building a Simple Course Recommendation system for online courses

## About the Project

This system is a minimalistic system built on the idea to help learners navigate through the courses on Coursera, aided by a data-driven strategy. Currently, this system only performs the task of identifying the most similar and most dissimilar courses to a selected course that is chosen by the learner from a pool of courses relevant to the skills the learner is interested in.

## Dataset Used

For the purpose of building this system, data from Coursera was scraped using the requests and beautifulsoup4 libraries. The `scraper.py` file contains code for scraping data from [https://www.coursera.org/courses](https://www.coursera.org/courses) and generates [coursera-courses-overview.csv]. The `course_scraper.py` file contains code to scrape details of each individual course and the output is [coursera-individual-courses.csv]

Both these above datasets have been combined to give [coursera-courses.csv]. This file consists of 1000 instances and 14 features and has a size of 1.41 MB.

### Features in the Dataset

The following features have been extracted for the dataset created above:

**course_url:** The URL to the course homepage  
**course_name:** The name of the course  
**learning_product:** The type of product that the instance is. It can be a course, professional certificate or a specialization. _(While all instances of the dataset are referred to as courses , this is not be confused with the learning_product of a particular instance)_  
**course_provided_by:** The organization/partner that is providing the course  
**course_rating:** Overall rating of the course  
**course_rated_by:** The number of students who have rated the course  
**enrolled_student_count:** The number of learners who have enrolled into this course  
**course_difficulty:** The difficulty level of the course. It can take values of beginner, intermeditae, advanced and mixed  
**skills:** The main skills that the course works at developing in a learner  
**description:** About the course  
**percentage_of_new_career_starts:** Percentage of learners who have had a new career start after completing this course  
**percentage_of_pay_increase_or_promotion:** Percentage of learners who have had a pay increment or received a promotion after completing this course  
**estimated_time_to_complete:** The estimated tome to complete the course  
**instructors:** The instructors taking the course

## What can this system do?

In a nutshell this system can perform the following tasks:

- Select courses for you based on the skills you want to learn
- Recommend courses that are most similar and dissimilar to the course you select
