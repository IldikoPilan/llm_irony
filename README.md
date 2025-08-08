# Description
This repository contains the data used in the paper: Margareta Berg, Ildikó Pilán, Ingrid Lossius Falkum and Pierre Lison. Pragmatic Reasoning for Irony Detection with Large Language Models in English and Norwegian. To appear in the _Proceedings of the SemDial 2025 Workshop Series on the Semantics and Pragmatics of Dialogue_.

Part of this material is adapted from a previous pragmatics experiment on irony and perspective-taking in children (Köder and Falkum, 2021), centered around simple situations involving a child and an adult. In the LLM-adapted version, each task was subdivided into two prompts: one consisting of a short context and a question about the adult speaker’s intent, and another containing the child’s action, the adult’s reaction and a question about the adult’s emotion. We added two follow-up questions for each task for investigating the presence of irony with LLMs: an indirect and a direct one. We complemented the original 12 stories with 24 new unique stories. The final dataset thus comprises 108 items derived from 36 unique stories, each associated with one of three possible outcomes: irony, praise, or criticism – the latter two representing non-ironic reactions.

References 

Franziska Köder and Ingrid Lossius Falkum. (2021). Irony and perspective-taking in children: The roles of norm violations and tone of voice. _Frontiers in Psychology_, 12:624604.

# Data structure
Each JSON file consists of a list of dictionaries with the following keys:
- _want_: sentences introducing the situation and asking about what the adult wants; 
- _emotion_: description of an even occurring followed by a question about the adult's emotion;
- _gold_label_: 'irony', 'praise' or 'criticism'; 
- _item_type_: 'original' if from the original study with human participants, 'original_with_new_condition' if the original story was re-written with a new condition, 'new' if the item was added for the LLM-based study;
- _item_id_: a running number identifying each item, consistent across the two languages.
