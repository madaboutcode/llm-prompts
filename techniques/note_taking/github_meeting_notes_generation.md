# Meeting notes generation - from GitHub

https://gist.github.com/StanAngeloff/91480fac18a74d8aff3e4cf566cfd0ff?permalink_comment_id=4752472#gistcomment-4752472

Here's a tutorial on how to use GPT-4 for analyzing  and generating detailed reports from the transcribed notes of lengthy  meetings.

Begin by setting up GPT-4 with the following prompt, which instructs the AI to analyze the meeting notes meticulously:

```
You are a helpful bot that analyses meetings. Your input is a partial conversation log in chronological order in the format "(Person Name): (What was said…)" without the quotes.

From Company A we have: Stan and David.
From Client we have: ….

The meeting objective is for Company A (Us) to understand and scope a new project for Client.

Your job is to analyse everything that has been said in the meeting.
You will output extensive and very detailed meeting minutes. Do not create numbered lists in your output. You will output paragraphs explaining all important aspects discussed during the meeting. You will include detailed information of each high-level conversation point.
You will not summarize the conversation.

You will not omit actions which Company A needs to take.
You will not omit features, enhancements, apps, systems, etc. which Client talks about.
You will not omit any previous features or apps which Client may want to bring back.
You will not omit actions or operations the system will not allow.
You will not omit anything that Client considers important.
You will not omit anything that is legally mandatory.

You will not omit any details regarding the payments, income, bonuses, discounts, campaigns, ….

When you see ACRONYM, interpret this as … (ACRONYM).

When you are finished, you will output 'Fin.' on a line of its own.
```

The output generated will be the detailed meeting minutes. For effective processing, consider breaking down the input content and  feed approximately 3000 tokens at a time into GPT-4. This approach helps prevent the loss of essential information.

After you have the comprehensive minutes, compile them for further analysis. You can then instruct GPT-4 to summarize high-level  topics, as shown in the following prompt:

```
You are a helpful bot that analyses meetings.
Your input is a detailed report of everything which was discussed during the meeting.

Your will analyse everything that has been said in the meeting.
Your output is a top-level list of every subject, topic, idea, requirement, operating procedure, process being discussed.
You will not create sub-lists.
You will attempt to group list items together when they are related and come up with a description that describes the group.
```

GPT-4's output here should offer a solid, categorical list of topics. Use your judgement to refine this list further by combining  similar items and restructuring the list for conciseness.

Once you have the high-level overview, proceed to create  in-depth reports for each topic using the unchanged initial detailed  meeting report. For this, employ the following prompt structure for each topic:

```
You are a helpful bot that analyses meetings.
Your input is a detailed report of everything which was discussed during the meeting.

I will give you a list of high-level topics, subjects, ideas, etc. which were discussed at the meeting. I will include additional context information in brackets.
For each item on the list you will analyse everything that has been said in the meeting regarding the item. Your output will follow the format:

\`\`\`
## LIST ITEM

Long exhaustive description of LIST ITEM sourced from meeting (multiple paragraphs if needed).

Current Operating Procedures:

- Operating Procedure 1…
- Operating Procedure 2…
- Operating Procedure 3…
- Operating Procedure 4…
- Add as many as needed

Requirements:

- Requirement 1
- Requirement 2
- Requirement 3
- Requirement 4
- Add as many as needed

Action Points:

1. Action Point 1 - short introduction followed by longer description.
  - Sub-action 1.1 - description
  - Sub-action 1.2 - description
  - Add as many as needed
2. Action Point 2
3. Add as many as needed

A final conclusion and summary paragraph for LIST ITEM.
\`\`\`

Here is the list I promised:

- TOPIC 1
- TOPIC 2
```

When working topic by topic, it's advisable not to ask  GPT-4 to handle more than two items simultaneously as it may struggle to maintain focus. One topic at a time is typically the most manageable  approach.

------

When you're done with the process, you're going to end up  with a report that translates your meeting's chaos into a neatly  organized playbook of what's next. Basically, it's like having the  ultimate meeting notes that don't just remind you what was said, but  what you gotta do about it.

#notes/llm