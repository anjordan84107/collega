# collega
Feature-based nearest-neighbor analysis framework

# Description
collegam (Latin, "colleague") provides a framework for doing feature-based nearest-neighbor analysis for any subject.

# Structure:
At a very high level, there are three elements:
- questions
- code used to answer the questions
- data used by the code to answer the questions

# Questions:
- A question is anything that we want to know about our subject.
- There are no bad questions; the idea is to keep this element focused on what we want to know without worrying about how (or even whether) the code will be able to answer the question.
- A question may be very defined (e.g., "is feature xyz present?") or it may be "fuzzy" (e.g., "does this instance of my subject look like a problem?")
- Questions may be organized into categories.  Conceptually, it is assumed that the quesitons in a category would be related in some way, but there are no actual restrictions on how a category is defined.
- Questions and categories are reflected by variables in config files.

# Code:
- Consists of a top-level script which invokes other scripts to handle the categories and questions.
- The code/script which handles a specific question should obviously try to "answer" the question.  But if/when a question can't be perfectly "answered", the script should simply try to provide helpful information.  Note that questions should be viewed as "sacred"; the process of implementing the code should never redefine a question.

# Data:
- The data consists of two pieces:
## the data associated with the current subject to be analyzed
## all the existing data that can be mined and compared against to answer the questions.
