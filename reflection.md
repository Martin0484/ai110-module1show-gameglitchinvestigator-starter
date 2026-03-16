# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
The game appeared to be normal at first. However, I noticed odd behavior from it as it ran. That's when I knew there were problems.
- List at least two concrete bugs you noticed at the start  
  (for example: "the secret number kept changing" or "the hints were backwards").
The game would keep on telling me to go higher even though the number was too large. I expected it to change output.
It would also keep on telling me to go lower even though the number was too small. I also expected it to change output.
Another bug is that it would not let me start a new game after playing just one game.

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
I used Copilot. I gave it context to help me debug the program in VsCode. I also carefully read its suggestions.
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
The AI suggested that I should change the outputs in the check_guess function. That was correct since the "Go HIGHER!" and "Go LOWER!" messages had to be swapped. I verified this suggestion by typing numbers in the game after I swapped the messages.
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).
The AI suggested that I must manually reset the session status to "playing". That was incorrect since I could use code to reset it in another way. I verified this by using code in app.py to reset the session.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
I ran the code and played the game by typing in various numbers. For example, sometimes I would type in high numbers and other times I would type in low numbers. I believe typing in a large variety of numbers helps with testing.
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
I ran a test to see if the bugs in check_guess had been fixed. The test showed me that the check_guess function was now giving the right messages based on the number provided by the user. If the number was too high, it would output "Go HIGHER!". If the number was too low, it would output "Go LOWER!".
- Did AI help you design or understand any tests? How?
AI helped me understand why the program did not start a new game when I clicked on "New Game" during one of my tests. It did this by providing me an explanation that mentioned multiple problems in the code. One problem was the session status not being updated.

---

## 4. What did you learn about Streamlit and state?

- In your own words, explain why the secret number kept changing in the original app.
The secret number kept changing because its value is created by using the randint method. The method creates a random number that is within a range. In this case, it gave a number from 1 to 100.
- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
Reruns are activated whenever a user interacts with a widget of the program. Session state helps preserve variables across different reruns. This helps prevent them from being lost when there is a rerun.
- What change did you make that finally gave the game a stable secret number?
I made sure the number was created randomly. This ensures that the number is random. Thus, it ensures the number is stable.

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
Use Copilot to help me debug programs in VsCode. This can help me reduce the amount of time I spend in debugging code. It can also help me understand problems in code better.
- What is one thing you would do differently next time you work with AI on a coding task?
Provide AI with more context. Examples of context include the purpose of the code and the name of the file containing the code. I think this will increase its chances of finding a good solution.
- In one or two sentences, describe how this project changed the way you think about AI generated code.
This project made me think of AI generated code as very useful but also confusing at times.
