# Conversational-AI
*Smart AI conversation system grounded on domain database*

**Step 1 : Speech to Text**
+ Tried open-source STT library `DeepSpeech` (streaming mode) and `Google STT` api (batch mode)

**Step 2 : Custom Entity and Intent Recognition using Transformers Model**

+ Data annotation for custom classes belonging to our entities and intents. 
+ Trained and tested different transformers models like `BERT`, `ConvBERT` etc.
+ Worked on the limitations of the BERT like models to improve the result.

**Step 3 :Belief State Tracking during Conversation**

+ Data annotation for our `belief state tracking` and `natural language response `
  along with entities and intents collected so far during the conversation.
+ `Vocabulary modification`,`T5 based tokenization` and converting the data into a suitable `.json` format for training
+ Trained and tested an open-source `T5 model` on the above data

**Step 4 :  Natural Language Question Generation**

+ For automatic querying SQL database grounded on intent,entity and belief state information,
  questions are generated in natural language which can be fed to the next step model which
  can write SQL query automatically.
  
**Step 5 : Automatic SQL Query Generation**

+ Tried different open-source `NLP2SQL` model to generate SQL Query just from natural language using `Semantic Parsing`.
+ Modified the open-source code in our favor and solved the issues faced during generating some
  complex query.
+ Fetching the required data from the database using the generated query.
  
**Step 6 : Final Natural language Response Generation**

+ Generaing final response for users grounded on actual data from the database

**Step 7 : Text to Speech**

+ Tried `pyttsx3` and `google speech api` to convert text into speech for end users

**Step 8 : Deployment**

+ Tried to build a `streamlit_webrtc` based web application for streaming audio input and output

