Notes and Comments for the Replication Package (data.zip) of the Manuscript “#ifdef Directives and Program Comprehension: A Study on Performance versus Perception” by Wolfram Fenske, Jacob Krüger, Maria Kanyshkova, and Sandro Schulze, accepted at ICSME 2020.
========================================================================================================================================================

Results
-------

The results are separated according to the code examples they refer to. Since each survey consisted of five code examples, there are five results files (in CSV format), encompassing the responses to questions Q8 to Q11 (see Table 2 in the paper for more information).

Columns & encoding:

* Columns mainly containing meta data
  * column 1: ID of participant
  * columns 2 to 4: the system the code example stems from, the ID of the snippet, and the position in the survey
  * column 5: lines that were hard to understand
  * column 11: just indicates whether the participant worked on an original or a refactored code example
  * column 16: indicates to which survey (S1 or S2) this answer belongs to

* Columns analyzed & discussed in the paper
  * column 6: CPP use appropriate? (Yes/No) —> refers to question Q10 in Table 2 of the paper
  * columns 7 to 10: relates to answers Q11-1 — Q11-45 in Table 2. Responses are given on a 4-point Likert scale with 1=very hard/difficult and 4=very easy

  * columns 12 and 13 (``comprehend1.idk`` and ``comprehend1.correct``): refers to question Q8 in Table 2 of the paper. Column 12 indicates whether the answer was “i don’t know”. If yes, then column 13 contains ``NA`` (for “no answer”), otherwise, column 13 indicates whether the selected answer for this question was correct (``true``) or incorrect (``false``).

  * columns 14 and 15: same as before, but for the second program comprehension question (i.e., question Q9 in Table 2 of the paper)


Participants
------------

In the file ``participants-data.csv``, we provide the metadata of our participants, i.e., the answers to questions Q1 to Q7 in Table 2 of the paper.

Columns & encoding:

* first column: ID of participant
* column 2: age of participant (refers to Q1 in Table 2), encoded as the concrete value (which is a period encompassing several consecutive ages; see PDF version of the surveys below)
* column 3: gender (Q2 in Table 2)
* column 4: general programming experience in years (Q3 in Table 2)
* column 5: C/C++ programming experience in years (Q4 in Table 2)
* columns 6 to 11: the various possible roles in software development projects (Q5 in Table 2). The last column contains the input of the participant if no predefined role was applicable.
* column 12: free text where participants specify which OSS projects they contribute to.
* columns 13 and 14: A self-assessment of participants about their programming skills in general (column 13) and in C/C++ in particular (column 14). Encoded as 4-point scale with 1=Beginner and 4=Expert (also see PDF version of surveys).
* column 15: indicates which survey (S1 or S2) the answer belongs to


Surveys
-------

For both surveys, we provide a PDF version. Note that the formatting is different from the online version. For example, some code examples are interrupted by a page break, which did not happen in the online version.


List of Repositories
--------------------

In the file ``list-of-repositories.pdf``, we provide a list of all the repositories for which we have sent emails to corresponding developers. In addition to listing the repository's name, we also indicate whether we have selected the repository based on previous work of Liebig et al. (ICSE 2010) or based on our own analysis of trending C repositories on GitHub.


R
-

The R archive comprises all R scripts and corresponding csv files we used to analyze the data and create the figures in our paper.