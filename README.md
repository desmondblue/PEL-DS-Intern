# PEL-DS-Intern
Temporary Database with following collections:
1. attempts: It holds summary data of student's attempt. Each test by a student becomes an attempt. If student takes 5 tests (same or different test), it will create 5 attempts. If student abandones the test, isAbandon flag is set to true. We consider only isAbandon = false documents. 

2. attemptDetails: Question level details such as time taken on each question can be found in this collection. Each attempt has a corresponding attemptDetails

3. practicesets: List of tests. Array 'questions' holds list of questions. Test can be created organically or can be created from the questions of question pool.

4. questions: list of questions. One question can be part of many tests. Question can be put in the pool using flag 'isAllowReuse'

5. grades/subjects/topics - master data of exam, related subjects and topics

6. users: list of students including teachers and parents

Problem Statement(s):
1. Does more practice mean better performance?
2. Detect fraud done by some test takers. Fraud can be based on
    - Number of consecutive correct answers
    - Time spent on each questions when answer is correct
    - Time spent outside the test window (offscreen time)
    - Time spent by other users of similar profile on this question
    - Strength and weakness of the student on the topic
    - Time spent by the student on similar questions
3. Student clusters based on different attributes e.g. performance, time spent, consistency, participation in discussion etc
4. A teacher may mark a question easy/medium/hard (Perceived hardness) but we want to give feedback to teachers on what's real hardness based on student's data (how many students answered correctly, how much time taken, whether student was good in the area/topic etc. )
5. Predict score in a test and challenge student to beat it 


Goal: To analyse the collections such as to provide solutions for the problem statements
