- 👋 Hi, I’m @vamsikumar824
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
vamsikumar824/vamsikumar824 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
class Question:
    def __init__(self,prompt,answer):
        self.prompt=prompt
        self.answer=answer
        

question_prompts=["What color are Apples?\n(a) Red/Green\n(b) Purple\n(c) Orange\n\n",
                  "What color are Bananas?\n(a) Teal\n(b) Magneta\n(c) Yellow\n\n",
                  "What color are Grapes?\n(a) Black\n(b) White/Green\n(c) Yellow\n\n"]

questions=[Question(question_prompts[0],'a'),
           Question(question_prompts[1],'c'),
           Question(question_prompts[2],'b')]
                     
def run_test(questions):
    score=0
    for q in questions:
        answer=input(q.prompt)
        if answer==q.answer:
            score+=1
    print('You got',str(score),'/',str(len(questions)),'correct')
    

run_test(questions)
