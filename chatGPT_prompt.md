Label a series of text-based messages. Each message needs to be labelled in isolation from one another and the label needs to be based on a codebook. Each message should have one or more labels. Where multiple labels are used the message should fit the requirements for each codebook entry. If a message has multiple labels then each label needs to be separated by a "/". Next to each label, you can provide a short explanation for why that label(s) was selected. The explanation needs to be concise and to the point.

Codebook in markdown table format

|Label | Category | Definition|
|:----|:----|:----|
|    doing | select/clarify | The  message is either a question that can be interpreted as `What are you doing?''   or a statement that can be interpreted as an answer to What are you doing?''|
|    why | select/clarify | The message is either a question that asks for information to justify why some action has (or has not) been taken or a statement that provides such a justification. The action can be an observation or a decision.|
|    features | select/clarify | The message (question or statement) specifically refers to features of an object or agent.|
|auto | select/clarify | Autocompleted messages used to share all sensed details for a given object via a button on the UI.|
|    dangerous | mutate/simulate | The message refers to actions / observations / decisions under an assumption that the object is dangerous.|
|    safe | mutate/simulate | As above but the assumption is the object is benign.|
|    make-safe | mutate/simulate | The message specifically refers to actions to make an object safe.|
|    order | dialogue/progress | The message is an order / instruction / command / tell.|
|    confirm | dialogue/answer | The message is a confirmation.| 

Example message entry and column names from a csv file

"id	group_size	message	label	comment"
"3591	52	Follow me	order	"
