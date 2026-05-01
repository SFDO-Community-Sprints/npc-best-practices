---
layout: default
title: Discovery Framework
nav_order: 3
parent: Industry Common Components
---
# Discovery Framework
Salesforce's Discovery Framework lets you build versioned, reusable question libraries for use with assessments tied to objects including Application Forms, Application Form Evaluations, Care Plans, Benefit Recertifications, Funding Awards, Funding Award Requirements, Individual Applications, Programs, Program Enrollments, Public Complaints or Referrals. 

Discovery Framework can be a valuable tool in scenarios where the questions themselves are a governed, reportable asset that needs to be reused consistently across the system. It is generally not a fit when you just need a quick form like an event RSVP, or an anonymous survey.

Typical use cases for Discovery Framework could include:


* Client and case intake assessments in human services, such as housing stability screenings, food security questionnaires, or domestic violence safety assessments


* Outcomes and impact measurement administered at intake, mid-program, and exit, where longitudinal comparison and reportability is valuable


* Volunteer screening and placement matching for sensitive roles such as mentoring, court-appointed advocacy, or working with minors and vulnerable adults
  
Good fits for Discovery Framework include:

* A need to track changes to individual questions over time. 


* A need to track change over time for individuals to understand how an engagement is impacting that individual.


* A need to standardize and reuse certain questions across different assessments, but also easily add questions for specific assessments.

Poor fits for Discovery Framework include:

* Lightweight forms like event registration, volunteer interest signups, or email list opt-ins, where a simple Screen Flow provides faster time-to-value

* Application Forms or similar single-use, large data intake forms which are better served by the Application Forms or Individual Application Objects

* Anonymous, high-volume feedback such as post-event surveys, donor NPS, or community listening campaigns, which Salesforce Surveys or FormAssembly handle better

* Complex grant scoring, ranking, and award decisioning logic - this is a potential use case for Business Rules Engine

* Conversational, unstructured, or open-ended client interviews for which the structured nature of the Discovery Framework would not be beneficial.  For use cases like this, explore a solution that combines some or all of Agentforce service agent capabilities with live agent workflow, depending on what is appropriate for the nature of the intake

Note and Considerations:

* Specialized functionality is available through Dynamic Assessments. Dynamic Assessments require different permissions and leverage distinct lightning components and Omniscripts. This documentation does not address that functionality.

* There is currently a known limitation preventing unauthenticated users from accessing assessments in AFNP orgs. 
