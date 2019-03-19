# Epics, User Stories and Acceptance Criteria
Once the requirements for a project have been determined, a Software Engineer can start to break down the project into logical subsets of features, at different levels of granularity.  
Epics, User Stories and AC are all user focussed, feature based methods of splitting up components of a project

## Epcis
Epics are high-level overviews of a large set of related features required from ONE perspective of a system. Epics and Epic Stories should:
* Focus on the features relevant to a single target user type
* Require an iterative process to be completed
* Be able to be broken down into smaller, more atomic units of work (User Stories)

## User Stories
User Stories are one of the most improtant primitives in Software Design. They describe a particular feature requirement from the perspective a single user, including the motivation behind the given feature. User Stories should:
* Narrate from the perspective of the user who desires the feature
* Efficiently describe the required feature
* Following the Role-Goal-Benefit (RGB) format, include the user, the feature and the motivation in a short summary
* Be able to be efficiently tested, or broken down into test cases

## Acceptance Criteria
AC are singular cases which describe one partiular action-outcome process from the perspective of a user. AC should:
* Be quantitative enough to be turned into actual test cases
* Be written from the perspective of a user (i.e. both the action and outcome are made by/for the user)
* Treat the system as a black box
* NOT include any specific design decisions which will be made by a developer