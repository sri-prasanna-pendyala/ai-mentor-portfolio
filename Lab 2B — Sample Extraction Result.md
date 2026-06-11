Input Resume

Candidate: Sri Prasanna Pendyala

Extracted JSON
{
  "name": "Sri Prasanna Pendyala",
  "email": "not_found",
  "phone": null,
  "education": [
    {
      "degree": "Bachelor of Technology in Computer Science",
      "institution": "Aditya Engineering College, Surampalem, India",
      "year": 2028
    },
    {
      "degree": "Diploma in Computer Engineering",
      "institution": "Aditya Polytechnic College, Surampalem, India",
      "year": 2024
    }
  ],
  "skills": [
    "C",
    "C++",
    "Java",
    "Python",
    "HTML",
    "CSS",
    "JavaScript",
    "ReactJS",
    "Bootstrap",
    "Node.js",
    "Express.js",
    "MongoDB",
    "MySQL",
    "Oracle",
    "Git",
    "GitHub",
    "Docker",
    "VS Code",
    "DSA",
    "OOP",
    "DBMS",
    "Operating Systems",
    "Computer Networks",
    "REST APIs"
  ],
  "projects": [
    "CodeVerse – Full-Stack Coding & Interview Preparation Platform"
  ],
  "experience_years": 0.5
}
Console Output
Loaded 3 sample resumes

Resume 1: Sri Prasanna Pendyala — 24 skills, 0.5 years exp

=== Full first result ===

{
  "name": "Sri Prasanna Pendyala",
  "email": "not_found",
  "phone": null,
  "education": [
    {
      "degree": "Bachelor of Technology in Computer Science",
      "institution": "Aditya Engineering College, Surampalem, India",
      "year": 2028
    },
    {
      "degree": "Diploma in Computer Engineering",
      "institution": "Aditya Polytechnic College, Surampalem, India",
      "year": 2024
    }
  ],
  "skills": [
    "C",
    "C++",
    "Java",
    "Python",
    "ReactJS",
    "Node.js",
    "MongoDB",
    "DSA",
    "DBMS",
    "OS",
    "CN"
  ],
  "projects": [
    "CodeVerse – Full-Stack Coding & Interview Preparation Platform"
  ],
  "experience_years": 0.5
}
Day 2 Lab 2B — Errors Handled
1. Markdown Fence Wrapping

Some LLM responses return:

{
  ...
}

instead of raw JSON.

The retry mechanism requests valid JSON only and re-validates using Pydantic.

2. Missing Phone Number

Many resumes do not contain a phone number.

Using:

phone: Optional[str] = None

allows the schema to validate successfully with null.

3. Empty Input

When an empty string is supplied:

extract_resume("")

Pydantic raises a ValidationError because required fields such as name and education are missing.

The caller catches the exception and reports the failure gracefully.
