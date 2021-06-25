# RASA-NLU---Chatbot

In this repository, we have built a chatbot that can answer questions related to Mucormycosis infection also colloquially called as Black Fungus infection.Mucormycosis is a deadly infection affecting the patients who have recovered from COVID-19 and currently very few people have knowledge about this deadly disease. The technology behind the chat is open source RASA X which internally uses Spacy library to process the Natural Language.The model was trained using DIET classifier in Tensorflow for 100 epochs.Furthermore, we were able to integrate the Chatbot into Telegram and Slack messaging application.Lastly, the application was deployed on Google Cloud Platform

Steps to install the chatbot

1. Create a virtual environment with python version 3.6. Rasa works only with python version 3.6,3.7,3.8 only.
2. Install rasa x (pip3 install rasa-x --extra-index-url https://pypi.rasa.com/simple).This may take a while.
3. Initialize the rasa using the command rasa init.Post rasa init, please run rasa shell to interact with bot.
4. Add your own intents in the file nlu.yml and add stories in the file stories.yml.Both of these files are present in data file.
5. After adding intents and stories, train the model using command rasa train.
6. Once trained successfully, hit the command rasa x to open the Rasa UI interface.
7. Converse with the bot and enjoy !

Screenshots:

![Screenshot from 2021-06-25 11-00-32](https://user-images.githubusercontent.com/45694329/123464806-ef6f5500-d60a-11eb-84f7-5e82dcb255d3.png)
![Screenshot from 2021-06-25 11-01-48](https://user-images.githubusercontent.com/45694329/123464823-f4cc9f80-d60a-11eb-9dd9-e1fb8a055dc1.png)
![Screenshot from 2021-06-25 11-02-35](https://user-images.githubusercontent.com/45694329/123464973-280f2e80-d60b-11eb-8642-8271b435cf62.png)
![Screenshot from 2021-06-25 11-03-29](https://user-images.githubusercontent.com/45694329/123464978-29d8f200-d60b-11eb-915a-9d302d0dc52c.png)
![Screenshot from 2021-06-25 11-06-47](https://user-images.githubusercontent.com/45694329/123465025-3b21fe80-d60b-11eb-9530-58cb72ff3ff9.png)

Steps to integrate the chatbot with Telegram and Slack.

1. To integrate the chatbot with Telegram first create a access token from Telegram BotFather and also create username.
2. Add the obtained access token and username in the credentials.yml file under telegram section
3. Finally add the webhook URL.To add webhook URL use ngrok.To create a URL using ngrok, use command ngrok http 5005
4. Run rasa using command rasa run.Additionally, at same time run rasa run actions to start the action server.
5. Go to telegram channel where bot is created and converse with bot.







Steps to integrate the chatbot with slack



