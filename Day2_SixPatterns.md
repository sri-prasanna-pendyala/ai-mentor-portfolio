Pattern 1 — PERSONA
Prompt
You are a senior placement coach at Aditya University. You have prepared 200 B.Tech CSE students for TCS, Infosys, and Cognizant placement interviews. A 3rd-year CSE student with 7.5 CGPA asks you about Big-O notation. Explain it the way you would in a 1-on-1 prep session — concrete, conversational, exam-relevant.
Output

Big-O notation is a way of measuring how an algorithm's running time or memory usage grows as the input size increases. Interviewers use it to judge whether you can analyze the efficiency of your code.

For example, if you search for a value in an array by checking each element one by one, the worst-case time complexity is O(n) because you may need to inspect all n elements. If you use binary search on a sorted array, the complexity becomes O(log n), which is much faster for large inputs.

For placements, remember the common complexities: O(1), O(log n), O(n), O(n log n), O(n²). When solving coding problems, always think not only about whether your code works but also about how efficiently it scales.

Self Score

4/5

Peer Score

8/10

Pattern 2 — FEW-SHOT
Prompt
Here are example explanations from a placement coach:

Q: What is recursion?
A: A function calling itself with a smaller problem. Like Russian dolls—open one, find a smaller one inside. Stops at base case. Example: factorial.

Q: What is a stack?
A: LIFO data structure. Push to add, pop to remove. Like a stack of plates—you take from the top.

Q: What is Big-O notation?
A:
Output

Big-O notation tells us how the running time of an algorithm grows as the input size increases. Think of it like estimating travel time for a road trip—the farther you go, the more time you need. For example, scanning every element in an array takes O(n), while binary search takes O(log n). Interviewers use Big-O to compare the efficiency of different solutions.

Self Score

5/5

Peer Score

9/10

Pattern 3 — CHAIN OF THOUGHT
Prompt
Explain Big-O notation to a placement interview candidate.

Think step by step before answering.

Step 1: Define Big-O in one sentence.
Step 2: Give one concrete example with code.
Step 3: Explain why interviewers ask about it.
Step 4: Synthesise into a 3-sentence summary.
Output

Step 1: Definition

Big-O notation describes how the running time or memory usage of an algorithm grows as the input size increases.

Step 2: Example

int sum(vector<int>& arr) {
    int total = 0;
    for(int i = 0; i < arr.size(); i++) {
        total += arr[i];
    }
    return total;
}

The loop runs n times, so the time complexity is O(n).

Step 3: Why Interviewers Ask

Interviewers want to know whether you can evaluate and optimize solutions. Two programs may produce the same output, but the one with better complexity is usually preferred.

Step 4: Summary

Big-O notation measures algorithm efficiency as input size grows. It helps compare different solutions to the same problem. Understanding Big-O is essential for coding interviews because it demonstrates problem-solving and optimization skills.

Self Score

4/5

Peer Score

8/10

Pattern 4 — STRUCTURED OUTPUT
Prompt
Explain Big-O notation for a placement interview.

Return ONLY valid JSON with this exact shape:

{
  "definition": "one-sentence definition",
  "intuition": "concrete analogy",
  "code_example": "Python snippet showing O(n) and O(n²)",
  "common_pitfall": "what students get wrong",
  "interview_test_question": "a follow-up question an interviewer might ask"
}
Output
{
  "definition": "Big-O notation describes how an algorithm's running time or memory usage grows as the input size increases.",
  "intuition": "Imagine counting students in a classroom. Visiting each student once takes O(n). Visiting every student and comparing them with every other student takes O(n²).",
  "code_example": "O(n): for i in range(n): print(i)\nO(n²): for i in range(n):\n    for j in range(n):\n        print(i, j)",
  "common_pitfall": "Students often focus on exact execution time instead of growth rate and forget to ignore constants.",
  "interview_test_question": "What is the time complexity of binary search and why?"
}
Self Score

5/5

Peer Score

10/10

Pattern 5 — SYSTEM PROMPT
System Prompt
You are a senior placement coach for B.Tech CSE students at an Indian engineering college. You prepare students for TCS, Infosys, and Cognizant interviews. You explain technical concepts in 50-80 words max, conversationally, with one concrete code example.
User Prompt
Explain Big-O notation.
Output

Big-O notation tells us how an algorithm scales as input size grows. For example:

for(int i = 0; i < n; i++) {
    cout << i;
}

This loop runs n times, so its complexity is O(n). In interviews, Big-O helps compare solutions and identify which algorithm performs better for large datasets.

Self Score

4/5

Peer Score

8/10

Pattern 6 — PROMPT CHAINING
Conversation 1 Output
1. Definition of Big-O
2. Common time complexities
3. Comparing algorithms
4. Space complexity
5. Importance in interviews
Conversation 2 Output

Definition of Big-O

Big-O notation measures how an algorithm's resource usage grows as input size increases.

Common Time Complexities

Common complexities include O(1), O(log n), O(n), O(n log n), and O(n²).

Comparing Algorithms

Big-O allows developers to compare multiple approaches and choose the most efficient one.

Space Complexity

Besides execution time, Big-O can also describe memory consumption.

Importance in Interviews

Interviewers use Big-O questions to evaluate problem-solving and optimization skills.

Conversation 3 Output

Big-O notation describes how an algorithm's running time or memory usage changes as input size grows. Common complexities include O(1), O(log n), O(n), and O(n²). It helps compare algorithms, evaluate efficiency, and understand scalability. Interviewers ask about Big-O because strong engineers must write solutions that work well for large inputs while using resources efficiently.

Practice Question: What is the time complexity of binary search, and why?

Self Score

5/5

Peer Score

10/10

Reflection

For my placement-prep students, the patterns I will use most are Persona Prompting and Prompt Chaining.

Persona Prompting helps generate explanations tailored specifically to engineering students preparing for placements. Instead of receiving generic textbook definitions, students get interview-focused guidance with practical examples.

Prompt Chaining is especially useful for DSA, DBMS, OS, and CN topics because it breaks a complex concept into smaller stages. First identifying subtopics, then expanding them, and finally summarizing them produces higher-quality explanations than a single large prompt. This approach also mirrors how students naturally learn difficult technical concepts.
