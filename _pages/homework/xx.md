---
permalink: 'hxx/'
title: Homework XX
when: 2024/11/04 - 5PM
reading:
  readings:
    - title: "AI dev"
      url: https://www.builder.io/blog/ai-dev-skill
    - title: "Hidden Cost of AI coding"
      url: https://addyo.substack.com/p/the-70-problem-hard-truths-about

programming:
  points: 10
  description: |
    ### Past or Future
    This assignment is an opportunity to experiment with the different communication strategies to connect an Arduino to a p5js sketch that we saw in class.

    We have a choice. We can either:

    - Pick a previous assignment and add a physical computing component to it.

      Maybe one of the first assignments we did could benefit from a potentiometer or a button. The drawing sketch of HW04B, or even some aspects of HW03A or HW03B could be parametrized to read an input from the Arduino.

      The physical input should change something significant about the sketch, not just colors.

    OR

    - Develop an early version of the communication aspect of our final project.

      This is a good moment to get started with the code for our final projects, and since communicating between an Arduino and p5js is a requirement, why not start there.

      This can be just about the data being shared between the two environments with a simplified version of the visuals or the final circuit.

      For example, if the project is a game with a custom controller, the focus will be on getting the signals from the Arduino to p5js to make an ellipse move. Or, if the final project uses 12 buttons to implement a super password machine, for now the task should be to get 2 or 3 of those buttons to communicate with p5js.

    ### Requirements and Considerations:
    - Pick one of the 3 strategies to connect an Arduino to p5js.
    - Bluetooth is the hardest.
    - Serial communication is symmetrical, the Arduino and p5js code for sending/receiving is very similar.
    - If adding a physical component to a previous assignment, the effect in p5js has to be more than just a change in color.
    - If not adding a physical component to a previous assignment, then this should be related to the final project.
    - Make a video showing the project working.
    - Include a README with:
      - A schematic drawing of the circuit.
      - Drawing of a Finite State Machine, if you have one.
      - Description of your logic.

    ### Submission and Grading:
    You can start by cloning one of these 3 templates, depending on which communication strategy you want to use: [Serial](https://github.com/DM-GY-6063-2024F-B/FinalProject-Serial), [WiFi](https://github.com/DM-GY-6063-2024F-B/FinalProject-WiFi), [BLE](https://github.com/DM-GY-6063-2024F-B/FinalProject-BLE).

    Use [Brightspace](https://brightspace.nyu.edu/d2l/home/407563) to submit a link to your repository and a video of your project working. The video should be about 1 minute long to show all the input/output signals being transferred between the Arduino and p5js. You can upload the file to Brightspace or host it somewhere else and submit a link.

    The following guide will be used for grading:

    | Task | Points |
    | --- | --- |
    | README file with circuit diagram | 2 points |
    | Follow assignment instructions | 2 points |
    | Implementation | 2 points |
    | Thoughtfulness | 2 points |
    | Craft | 2 points |

    Implementation: work shows evidence of understanding programming concepts and you are fully using them to express your ideas.

    Thoughtfulness: project demonstrates your personality and it's not a straightforward re-implementation of someone else's idea.

    Craft: code and results show care and consideration for presentation and professionalism, and work doesn't look like it was rushed.

reading:
  points: 5
  title: Media as environment, or environment as media? How are the natural and the media worlds entangled?
  intro: "Write a 200-word response to the following:"
  description: |
    Feel free to read all of the pages suggested, or, after reading the Introduction (pages 1 - 13), pick one of the four chapters (chapters 2, 3, 4 or 5) and read the first few pages, as listed above.

    Access [Worlds In Figures](https://worldsinfigures.com), watch the tutorial video and play with the software.

    As always, your response should be personal, meaning that you should be expressing your views and opinions about the text and not just summarizing it. You can use the following rubric to guide your response:

    - Short summary: in one or two phrases, what is the text about?
    - Short summary: in one or two phrases, what is Evan Roth's project about?
    - How is Evan Roth's project related to the text?
    - Which chapter of the book did you pick? What is it about?
    - Memorable quote: Is there a phrase in the text that stands out or captures the main idea of the text?
    - Did you learn something new? What?
    - What do you agree or disagree with? Why?
    - How is this text related to programming?
    - Is the text related to any of the other readings we've done so far?

    Please submit your response via [Brightspace](https://brightspace.nyu.edu/d2l/home/407563).

    Alternatively, you may create a ```reading.md``` file in your HW12 repo and write your response in markdown. Just make sure to submit a link to the file using [Brightspace](https://brightspace.nyu.edu/d2l/home/407563).

    Grading for the readings will be assigned following these considerations:

    | Response | Grade|
    | --- | --- |
    | Only summarized the reading | 1 point |
    | Summarized the reading and project | 2 points |
    | Answered some of the prompts, but I can't tell whether<br>you actually read the text and saw the project | 3 points |
    | Answered enough prompts to express opinions | 5 points |
  readings:
    - title: "The Marvelous Clouds: Toward a Philosophy of Elemental Media"
      author: John Durham Peters
      url: https://brightspace.nyu.edu/d2l/common/viewFile.d2lfile/Database/MjA5MTA0ODU/peters_marvelous-clouds.pdf?ou=312200
      chapter: Introduction and one of chapters 2, 3, 4, 5
      pages: 1 - 13, 53 - 57, 115 - 119, 165 - 169, 213 - 218
    - title: Worlds In Figures
      author: Evan Roth
      url: https://worldsinfigures.com/tutorial
      chapter: Tutorial and Software


reading:
  points: 5
  title: What is media archaeology?
  intro: "Keep this question in mind while you read and write a 200-word response to the following:"
  description: |
    The sections to read are:
    - Introduction ETHER/ORE (pg vii)
    - Building Hudson Yards (pg vii)
    - Our Materials of Investigation (pg xxxv)
    - Waves and Wires CITIES OF ELECTRIC SOUND (pg 1)

    As always, your response should be personal, meaning that you should be expressing your views and opinions about the text and not just summarizing it. You can use the following rubric to guide your response:

    - Short summary: in one or two phrases, what is the book about?
    - Memorable quote: Is there a phrase that stands out?
    - Did you learn something new? What?
    - What do you agree or disagree with? Why?
    - Did the text remind you of any other texts we've read so far?
    - How is the text related to programming?
    - Was there anything in the text that surprised you? What? Why?

    Please submit your response via [Brightspace](https://brightspace.nyu.edu/d2l/home/407563).

    Alternatively, you may create a ```reading.md``` file in your HW11 repo and write your response in markdown. Just make sure to submit a link to the file using [Brightspace](https://brightspace.nyu.edu/d2l/home/407563).

    Grading for the readings will be assigned following these considerations:

    | Response | Grade|
    | --- | --- |
    | Only summarized the reading | 2 points |
    | Answered some of the prompts, but I can't tell whether<br>you actually read the text, or what you thought | 3 points |
    | Answered enough prompts to express opinions | 5 points |
  readings:
    - title: Code and Clay, Data and Dirt
      author: Shannon Mattern
      url: https://brightspace.nyu.edu/d2l/common/viewFile.d2lfile/Database/MjA3MjAzMTY/mattern_code-clay-data-dirt.pdf?ou=312200
      chapter: Introduction and Chapter 1
      pages: vii - xii, xxxv - xl, 1 - 5


reading:
  points: 5
  title: Other codes and other technologies
  intro: "Read and write a 200-word response to the following:"
  description: |
    Just to avoid confusion, the sections to read are called:
    - Introduction: The New Jim Code (pg 9)
    - Everyday Coding (pg 10)
    - Move Slower ... (pg 15)
    - Tailoring: Targeting (pg 20)
    - Race as Technology (pg 33)

    As always, your response should be personal, meaning that you should be expressing your views and opinions about the text and not just summarizing it. You can use the following rubric to guide your response:

    - Short summary: in one or two phrases, what is the book about?
    - Memorable quote: Is there a phrase that stands out?
    - Did you learn something new? What?
    - What do you agree or disagree with? Why?
    - Did the text remind you of any other texts we've read so far?
    - How is the text related to programming?
    - Was there anything in the text that surprised you? What? Why?

    Please submit your response via [Brightspace](https://brightspace.nyu.edu/d2l/home/407563).

    Alternatively, you may create a ```reading.md``` file in your HW10 repo and write your response in markdown. Just make sure to submit a link to the file using [Brightspace](https://brightspace.nyu.edu/d2l/home/407563).
  readings:
    - title: Race After Technology
      author: Ruha Benjamin
      url: https://brightspace.nyu.edu/d2l/common/viewFile.d2lfile/Database/MjA1NzUyNTI/benjamin_race-after-technology.pdf?ou=312200
      chapter: Introduction
      pages: 9 - 23, 33 - 36

reading:
  points: 5
  title: One Last Reading !
  intro: "Write a 200-word response to the following:"
  description: |
    As always, your response should be personal, meaning that you should be expressing your views and opinions about the text and not just summarizing it. You can use the following rubric to guide your response:

    - Short summary: in one or two phrases, what is the text about?
    - Memorable quote: Is there a phrase in the text that stands out or captures the main idea of the text?
    - Did you learn something new? What?
    - What do you agree or disagree with? Why?
    - How is this text related to programming?
    - Is the text related to any of the other readings we've done so far?

    Please submit your response via [Brightspace](https://brightspace.nyu.edu/d2l/home/407563).

    Alternatively, you may create a ```reading.md``` file in a GitHub repo and write your response in markdown. Just make sure to submit a link to the file using [Brightspace](https://brightspace.nyu.edu/d2l/home/407563).

    Grading for the reading will be assigned following these considerations:

    | Response | Grade|
    | --- | --- |
    | Only summarized the reading | 1 point |
    | Answered some of the prompts, but I can't tell whether<br>you actually read the text | 3 points |
    | Answered enough prompts to express opinions | 5 points |
  readings:
    - title: "The Question Concerning Technology in China"
      author: Yuk Hui
      url: https://brightspace.nyu.edu/d2l/common/viewFile.d2lfile/Database/MjExMzI2ODY/hui_question-concerning-technology-china.pdf?ou=312200
      chapter: Introduction
      pages: 1 - 17

---
{% include homework.html homework=page %}

<script src="{{ site.baseurl }}/assets/simplelightbox/simple-lightbox.min.js"></script>
<script src="{{ site.baseurl }}/js/lightbox.js"></script>
