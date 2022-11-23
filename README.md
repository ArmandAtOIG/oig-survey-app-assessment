# oig-survey-app-assessment
Coding assessment for new developers @ OIG

## Introduction
Thank you for taking the time to give us an insight into your development style. In this short assignment, we ask you to build a small application based on what you might encounter when joining OIG. In our next meeting, we will discuss which approaches you used and what decisions you made.

Make sure that you can show a working prototype of the application.

## The application
Create an application in which the end-user can plan and manage questionnaires. A questionnaire in this context is a
means of gathering answers to questions online on a large scale.

### Prerequisites
- The application is built on either the latest .NET framework or .NET. 
- You should use.NET MVC (the.Net framework) or Blazor.
- You can use any CSS component framework of your choice. Prioritize functionality over looks.
- You use some sort of architecture approach, and you are not allowed to inject your DB context directly into a controller as this would immediately disqualify your application. 
- You can use a database or code first. Note that you will need to explain your decision.
- Diagrams should be available for:
- A high-level diagram depicting the use case and how your application resolves the issue
  - Database diagrams illustrating entities and relationships
- The application should be run within a Docker image.
- Data is persisted to some sort of data store. Please keep in mind that you must explain your storage preference.
- Provide a diagram of how you would host your application on Azure and be able to explain your choices.

### Use-cases
The following use cases are the foundation for the application:
- As a system user, I want to be able to schedule a questionnaire so that I can ask my target group about a
topic/case.
- As the owner of a scheduled questionnaire, I want to be able to reschedule the questionnaire as long as it has
not started.
- As the owner of an active questionnaire, I want to be able to close the questionnaire at will.

### Static structure
A questionnaire should at least consist of the following:
- Name
- Startdate/time
- Enddate/time
- Status

### Business rules
The following business-rules are applicable:
- A questionnaire can only be scheduled for a future date/time.
- No "retroactive" changes are allowed.
A questionnaire is planned for the future and will be completed in the future.
- The end date and time are at least one hour after the beginning date and time.
- A questionnaire will always exist in one of the following states:
- Concept: The questionnaire is intentionally inactive, and cannot be administered.
- Scheduled: The start date and time of the questionnaire are in the future. No questions can be answered yet.
Active: the questionnaire's start date and time are in the past, while its end date and time are in the future. Only in this state can the questions be answered.

- Completed: The questionnaire's end date and time have passed. No more questions can be answered.

The mentioned statuses are sequential, never skip a step, and cannot be reversed.

### Interface
Build at least the following screens:
- Create-screen for a questionnaire
- Update-screen for a questionnaire
- Overview-screen of questionnaires
  - Display at least the name, startdate/time and enddate/time
  - Sort the overview-screen by startdate/time, enddate/time (by default)
  - Create an intuitive search-function for questionnaires
- A stub for the "answering-screen"; it is in this stage sufficient to display the questionnaire status.

### Non-functionals
- Create or use a pleasant user experience for the end user. Keep it simple but attractive. Explain briefly.
- Document the application as you see fit, make your own estimate of what should and should not be
documented, to what extent, and in what way.

### System design
You do not need to create a tangible product as an answer to the following questions; this is about making an
"exploratory" system design. Take your time to think about these points, we will use this as discussion material in the
conversation.
- Think about how you would have a respondent fill out the questionnaire.
- How would you make the technical setup to show a respondent the questionnaire?
- What data do you use for this?
- How do you communicate with the respondent?
- In certain cases, not all respondents are registered in the system in advance. For example, if you want to conduct
a questionnaire via a link on a website. How would you arrange that?

## Working with Github

Please fork the repository to your account, add armand.jordaan@oig.nl.com as a collaborator, and add a commit message indicating you have started the assessment. Once completed, please let us know so we can schedule the next phase.


## Time Restriction

Ideally, you should be able to deliver this assessment within 48 hours of starting it. The objective is to add a time constraint to assess how much you can get done, where you cut corners, and why.


## Finally
We understand that you can fill in certain parts of the above specifications as liberally or strictly as you desire. We would
Therefore, I would like to offer you the following:
- "As the owner of a questionnaire,"  ownership and the associated plumbing are a lot of work. It is sufficient to
deliver the application without a security solution.
- It is sufficient to show a working prototype of the application with the requested functionality implemented.
Of course, it does not have to be a fully fledged, production-worthy application.
- Feel free to show off your special skills and how you can apply them here.
- If you feel the need to elaborate a little further than "strictly necessary" for demo purposes or to show a
neat/beautiful/unexpected feature, we would of course appreciate that.
- If the above takes an unreasonable amount of time, the decision of what to implement and what to skip is at your discretion. However, if you do skip a feature or a requirement, we want to know why and what trade-offs and implications you considered.
- If you have any questions, don't hesitate to contact us.

Thank you in advance, and I hope to speak with you soon!
Onderwijs Innovatie Groep
