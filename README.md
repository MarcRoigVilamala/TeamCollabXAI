# TeamCollabXAI

Repository for the messages sent during human-AI experiments labelled using an explainable AI (XAI) framework.

This repository contains three documents, detailed in the following sections.

## Group annotations

**group_annotations.csv** contains the manual and ChatGPT labels for the selected repesentative human messages for each group of *similar* messages sent during the experiments. The columns of this file show:

- **id** of the representative message.
- **group_size**, indicating the size of the group of *similar* messages.
- **message**, the text content of the representative message.
- **annotators a to d**, showing the labels given by each of the 4 human annotators.
- **ChatGPT**, showing the labels assigned by ChatGPT4o for that message.
- **merged_label_w_ChatGPT**, showing any labels assigned by 3 or more annotators, including labels assigned by ChatGPT.
- **merged_label_w/o_ChatGPT**, showing any labels assigned by 3 or more annotators, with ChatGPT exlcuded. *This is the ground truth considered in the paper.*

## Labelled Messages

**labelled_messages.csv** contains all the original messages sent during the experiments, including both human and AI messages. All messages are shown in temporal order for each session. The columns on this file show:

- **id** of each message.
- Session details, including:
  - **session**, the identifier for each session.
  - **strategy**, the strategy agents were asked to follow for that session.
  - **substrategy**, the substrategy agents were asked to follow for that session.
- Sender details:
  - **sender**, the agent who sent the message.
  - **agent_type**, the type of agent who sent the message (human or AI).
  - **role**, the role of the agent who sent the message (order or obey for hierarchical sessions, sensing or lifting for complementary sessions, independent for other sessions).
- Receiver details:
  - **receivers**, the list of agents who received the message.
  - **human_receivers**, which indicates the subset of receiver agents who are also humans.
  - **ai_receivers**, which indicates the subset of receiver agents who are also AI.
- Message details:
  - **time** in seconds after the start of the session when the message was sent.
  - **message**, the content of the message.
  - **label_w/o_ChatGPT**, showing the merged labels for human messages according to annotators (ChatGPT excluded). *This is the ground truth considered in the paper.*
  - **label_w_ChatGPT**, showing the merged labels for human messages according to annotators (ChatGPT included).

## ChatGPT Prompt

**chatGPT_prompt.md** contains the prompt given to ChatGPT4o asking it to label the messages.
