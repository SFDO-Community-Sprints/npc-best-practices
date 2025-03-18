---
title: Program & Case Management
parent: NPSP to NPC Translations
nav_order: 5
---
# Program & Case Management 
<table>
<tr>
 <td><strong>Capability</strong>

   </td>
   <td><strong>PMM</strong>

   </td>
   <td><strong>Nonprofit Cloud</strong>

   </td>
   <td><strong>Best Practices Group Notes</strong>

   </td>
   <td><strong>Examples</strong>
   </tr>
  <tr>
   </td>
   <td>Track overarching themes, areas of focus, departments, or programs

   </td>
   <td>Program

   </td>
   <td>Program

   </td>
   <td>Programs are overarching themes, areas of focus, or departments that make up your organization's mission. These are the foundational base for your reporting.

   </td>
   <td>Job Readiness

After-School Program

Family Support Program
</tr>
<tr>
   </td>
   <td>Track services, events, workshops, opportunities, or resources that people can access or receive for each Program

   </td>
   <td>Service

   </td>
   <td>Benefit

   </td>
   <td>Benefits are the things that your organization does that make up your Programs. They are all the services, events, workshops, and opportunities that people can access or resources that people can receive.

   </td>
   <td>Bus Passes

Financial Stipend

1:1 Mentoring
</tr>
<tr>
   </td>
   <td>Track the frequency that a service will be delivered, either as a single or recurring set of sessions. Participants can be added to schedules if they are to receive a benefit on a regular basis.

   </td>
   <td>Service Schedule

   </td>
   <td>Benefit Schedule

   </td>
   <td>Benefit Schedules are planned instances of the benefit, typically used to track a series of workshops or an event, or the frequency that a service will be delivered. Schedules can be a single session or a recurring schedule of sessions.

   </td>
   <td>A food pantry offers open food shopping every Monday from 5:00-7:00 PM

A social services agency distributes bus passes to clients on the 30th of every month
</tr>
<tr>
   </td>
   <td>Track individual instances or sessions of a service/benefit

   </td>
   <td>Service Session

   </td>
   <td>Benefit Session

   </td>
   <td>Benefit Sessions are a single instance of a benefit schedule, such as an event, class or workshop. A related Benefit Schedule is required to use a Benefit Session. The benefit session represents an instance of a planned benefit delivery and the date and time it will occur.

   </td>
   <td>The specific instance of the date/time that a food pantry operated it's open shopping hours
</tr>
<tr>
   </td>
   <td>Enroll an individual in a program

   </td>
   <td>Program Engagement

   </td>
   <td>Program Enrollment

   </td>
   <td>People who are enrolled or are a part of a specific Program. This allows them to register and participate in Benefits that are a part of the related program.

   </td>
   <td>A senior registers and enrolls for a meal-delivery service program
</tr>
<tr>
   </td>
   <td>Assign an individual to a service/benefit

   </td>
   <td>Service Participant

   </td>
   <td>Benefit Assignment

   </td>
   <td>A record that stores the association between a benefit and a participant. Connects to the Benefit. Requires a parent record (Program Enrollment, Care Plan, Goal Assignment, or Individual Application). Can be used to track ad hoc interactions. The Benefit Assignment represents a benefit that the client is entitled to receive. It may also include an entitlement amount that the client is entitled to receive. The Benefit Assignment can be infinite or it might have a defined start and end date after which the eligibility to receive the benefit expires.

   </td>
   <td>A senior registers and enrolls for a meal-delivery service program and receives a benefit assignment for meal delivery. The meal deliveries will be fulfilled on an ongoing basis with no defined end date.

A participant in the employment program is assigned and entitled to 10 sessions of job coaching.
</tr>
<tr>
   </td>
   <td>Track and individual's enrollment in a specific Service/Benefit Schedule

   </td>
   <td>Service Participant

   </td>
   <td>Benefit Schedule Assignment

   </td>
   <td>A record that represents a participant's enrollment to a Benefit Schedule.

   </td>
   <td>A Youth Development organization has an afterschool program that meets on Mondays at 6pm or Wednesdays 6pm. A participant who selects the Monday schedule will have a benefit schedule assignment record that connects them to the program schedule for Monday's at 6:00pm.
</tr>
<tr>
   </td>
   <td>Track delivery of a service/benefit/resource

   </td>
   <td>Service Delivery

   </td>
   <td>Benefit Disbursement

   </td>
   <td>A recording of when a benefit is given to a participant (and optionally, how much). Benefit disbursements are the backbone of reporting who received benefits from your organization and when they received them. You cannot have a Benefit Disbursement without a Benefit Assignment.

   </td>
   <td>Student receives tutoring at a session. A participant receives a bus pass allocated to them
</tr>
<tr>
   </td>
   <td>Define categories of benefits and link to their units of measure

   </td>
   <td>
   </td>
   <td>Benefit Type

   </td>
   <td>Benefit types categorize benefits into buckets such as monetary, services or goods, however, benefit types can alternatively be used to categorize benefits by an organization's areas of focus. Regardless of how they are configured, benefit types offer a way to categorize benefits into categories that are meaningful for the organization, so they may report on how their benefits distributed across programs. Benefit Types are the Parent record to Benefits, so downstream sharing rules are inherited from the Benefit Type.

   </td>
   <td>A Youth Development organization offers classes and workshops to help students prepare for college, and scholarships and student stipends to pay for books. They have a benefit type called Monetary to track benefits for scholarships and stipends, and they have a benefit type called Education, to track all benefits related to courses and training.

Alternatively, a Music School offers a multitude of classes and programs for various musical activities and courses. They use the following benefit types to categorize their courses by instrument: Flute, Clarinet, Piano, and Percussion. The corresponding benefits under each category are the various classes offered in that instrumental area, e.g. Intro to Flute, Flute Level 1, and Flute Level 2.
</tr>
<tr>
   </td>
   <td>Defines the units and systems of units used to express and account for quantities

   </td>
   <td>
   </td>
   <td>Unit of Measure

   </td>
   <td>Unit of Measure helps to standardize reporting and grouping of benefits with specific types of metrics, such as time, volume, or quantity

   </td>
   <td>Dollars ($)

Sessions

Hours
</tr>
<tr>
   </td>
   <td>Group program enrollees together based on criteria

   </td>
   <td>Program Cohort

   </td>
   <td>Program Cohort

   </td>
   <td>A cohort groups program enrollments together based on factors like start date, location, program type, or other relevant criteria.

By creating cohorts, you can easily monitor the progress of a group of participants through the program lifecycle, analyzing metrics like attendance, completion rates, and outcomes

   </td>
   <td>Summer youth program:

A cohort could represent all the teenagers enrolled in a summer youth development program starting in June.

Job training program:

A cohort could be a group of individuals starting a specific job training course on the same date
</tr>
<tr>
   </td>
   <td>Track members of a program cohort

   </td>
   <td>
   </td>
   <td>Program Cohort Member

   </td>
   <td>Indicates the individual that is a member or enrollee of a specific Program Cohort

   </td>
   <td>Summer youth program:

A program cohort member represents the individual's membership in the cohort.
</tr>
   </td>
   </table>
