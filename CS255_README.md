# CS 255: System Analysis and Design – Portfolio README

**Student:** Ariful Wadud
**Course:** CS 255 – System Analysis and Design
**Institution:** Southern New Hampshire University

---

## Portfolio Artifacts

This repository contains the following deliverables from CS 255:

- `CS_255_Business_Requirements_Document.docx` – Project One: Business requirements gathered from the DriverPass client interview, including functional requirements, nonfunctional requirements, system background, objectives, assumptions, and limitations.
- `CS_255_System_Design_Document.docx` – Project Two: Full system design including UML Use Case, Activity, Sequence, and Class diagrams, along with technical requirements covering hardware, software, security infrastructure, and deployment tools.

---

## Reflection

### Briefly summarize the DriverPass project. Who was the client? What type of system did they want you to design?

The client was DriverPass, a company founded to address a widespread problem: the majority of students who take driving tests fail on their first attempt. DriverPass wanted a web-based system that would give students better tools to prepare — specifically online practice exams, on-road lesson scheduling, and progress tracking. The system also needed to serve instructors, who would manage lesson schedules and update training records, as well as administrators and IT staff who would handle user accounts, system maintenance, and reporting. The goal was to build a secure, accessible platform that could be used from any modern browser or device, reducing the friction between students and the preparation resources they needed.

### What did you do particularly well?

I think the area where I was strongest was translating the client's spoken needs from the interview transcript into structured, actionable requirements. Rather than just listing surface-level features, I worked to understand the intent behind each request — for example, recognizing that the client's concern about security wasn't just about passwords but about role-based access, account lockouts, and encrypted data transmission. I captured that nuance clearly in both the functional and nonfunctional requirements sections. On the design side, the class diagram came together well, with a clean inheritance hierarchy rooted in an abstract User class and meaningful associations between Student, Lesson, PracticeExam, and ExamResult that accurately reflect how data flows through the system.

### If you could choose one part of your work on these documents to revise, what would you pick? How would you improve it?

If I could revise one part, it would be the activity diagrams. While both diagrams accurately represent their core workflows, they could go deeper on error handling and edge cases. For example, the scheduling diagram handles the case where a time slot is unavailable, but it does not capture what happens if the student's session times out mid-booking, or what occurs when the system encounters a database error during the save operation. In a real development environment, developers need that level of detail to write robust code. I would revise both activity diagrams to include additional decision branches for exception scenarios, making them more complete and practical for implementation.

### How did you interpret the user's needs and implement them into your system design? Why is it so important to consider the user's needs when designing?

Interpreting user needs started with a careful reading of the client interview transcript, where I paid attention not just to what was explicitly requested but also to the underlying problems being described. When the client mentioned that students were failing tests at high rates, that pointed directly to what the system needed to do: provide targeted, accessible practice. I organized those needs into formal functional requirements ("The system shall allow students to take online practice exams") and nonfunctional requirements covering accessibility, security, and performance — giving the development team clear, traceable targets.

Considering user needs is fundamental to good system design because a technically flawless system that solves the wrong problem is worthless. If the system had been optimized for administrator reporting at the expense of the student experience, it would fail at its actual purpose. Users are the people who ultimately determine whether a system succeeds or fails in practice. Designing from their perspective — what they need, how they think, what would frustrate them — is what transforms a set of technical requirements into a product that delivers real value.

### How do you approach designing software? What techniques or strategies would you use in the future to analyze and design a system?

My approach starts with understanding before designing — spending time with the problem space, the client's goals, and the constraints before drawing a single diagram or writing a single requirement. For analysis, I rely on structured interviews and careful documentation to surface both explicit needs and implicit expectations. I then use UML diagrams iteratively: starting with a use case diagram to map the scope and actors, moving to activity and sequence diagrams to trace workflows in detail, and finally building the class diagram as a structural blueprint once the behavioral logic is clear.

Going forward, I plan to lean more heavily on iterative feedback loops during the design phase — sharing early drafts of diagrams with stakeholders before committing to a direction, since assumptions made early can be expensive to undo later. I also want to be more deliberate about designing for change: using patterns that keep the system flexible, such as role-based access control that can accommodate new roles without restructuring the codebase, rather than optimizing only for current requirements. Finally, I would ensure that every design decision is traceable back to a specific requirement, so that developers and reviewers can always understand why something was designed a particular way, not just what was built.
