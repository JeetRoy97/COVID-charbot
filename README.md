
**Assignment- Covid Chatbot**

To implement the chatbot model, we have used RASA 2.0, which is an open-source toolkit for developing a chatbot. 

There are five important contents in RASA chatbot creation viz. NLU data, responses, stories, forms and rules. These are store in .yml format. 

\1. Using the nlu.yml file, the assistant understands how the user express its needs using the phrases. These examples are grouped together on the basis of the expressions, called as intent. These intents and examples are used for training the assistant’s Natural Language Understanding (NLU) model. A glimpse of out NLU model is shown in figure below:


Fig 1: nlu.yml showing intent and examples

\2. Using responses stored in the domain.yml file, the assistant respond back to the user. If there are multiple options in the responses, then it chooses randomly. A sample reesponse is shown in the figure below:


Fig 2: responses in the domain.yml file

\3. The story.yml file shows the intent and actions taken on each user messages. This story shows the conversational workflow of each to accomplish the goal.

Fig 3: stories.yml file representing the intents and respective actions

\4. If the assistant need to collect relevant information from the user, then it is performed using the forms.

\5. The rules.yml file represent the path in which the conversation proceeds when the assistant corresponds to specific action mapped to the intent.

**Dataset-**

The task assigned is to design a chatbot model for COVID assistance. We have been provided with a question-answer pair .xlsx file.

Pre-processing-

In the pre-processing steps, we separate the question-answer pairs in nlu.yml and domain.yml file. The connection between the question and answer is established using stories.yml. 


Fig 4: Pre-processing of dataset into separate yml files. 


**Data- Augmentation-**

As we have lack of training data, we may fail to give quality results. So, to improve the dataset, we augment the questions, using Google related search questions. We have written a .py script for this augmentation. 

Fig 5: Augmented questions

Fig 6: Augmentation using the Google related search queries


**Results-**


Fig 7: Chatbot conversations







Fig 8: Chatbot conversations


In some conversations, the chatbot answer good responses but in some it fails to give correct results due to lack of domain knowledge. In the following example, it failed to give correct result for the last phrase as it has no domain knowledge related to flight services. 




` `This can further be more improved by making robust against new questions. This can be achieved by increasing more knowledge about the topic.

