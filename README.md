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
![Screenshot from 2021-06-25 11-06-47](https://user-images.githubusercontent.com/45694329/123465025-3b21fe80-d60b-11eb-9530-58cb72ff3ff9.png)

Steps to integrate the chatbot with Telegram and Slack.

1. To integrate the chatbot with Telegram first create a access token from Telegram BotFather and also create username.
2. Add the obtained access token and username in the credentials.yml file under telegram section
3. Finally add the webhook URL.To add webhook URL use ngrok.To create a URL using ngrok, use command ngrok http 5005
4. Run rasa using command rasa run.Additionally, at same time run rasa run actions to start the action server.
5. Go to telegram channel where bot is created and converse with bot.

Telegram integration screenshot
![Screenshot](https://user-images.githubusercontent.com/45694329/123465886-52152080-d60c-11eb-903c-eab4a770f22a.jpg)
![ss](https://user-images.githubusercontent.com/45694329/123466238-bfc14c80-d60c-11eb-9a29-454cee618b9c.jpg)

Steps to integrate the chatbot into slack.[1]
1.First create the app in slack and integrate the chatbot into the app (app.slack.com/apps)
2.Add the Slack token key, app ID and secret key in the domain.yml file
2.After creating the app in slack, run the command rasa run.
3.Open the slack app, converse with the bot in the apps section of the slack.

Slack integration screenshot
![Screenshot from 2021-06-25 17-57-42](https://user-images.githubusercontent.com/45694329/123466690-41b17580-d60d-11eb-840a-9a761626d9c1.png)
![Screenshot from 2021-06-25 18-04-22](https://user-images.githubusercontent.com/45694329/123466705-4544fc80-d60d-11eb-897a-d5ee8f81881b.png)

Steps to deploy the model into Google cloud platform [2]

1.Create a new VM instance in the GCP.Minimum configuration include 4 GB RAM, Ubuntu 20.04 LTS, 50 GB HDD in GCP.
2.Install the Rasa X in the created VM instance.Set the password for RASA login.
3.Once installed link the RASA in GCP with the GIT hub repository
4.Train the model and then converse with chatbot.

Google Cloud Platform Screenshot

![Screenshot from 2021-06-25 20-50-15](https://user-images.githubusercontent.com/45694329/123467399-18ddb000-d60e-11eb-9659-5b9477fe76d4.png)
![Screenshot from 2021-06-25 20-20-28](https://user-images.githubusercontent.com/45694329/123467378-1418fc00-d60e-11eb-80e3-fb467ba33022.png)
![Screenshot from 2021-06-25 20-21-06](https://user-images.githubusercontent.com/45694329/123467392-167b5600-d60e-11eb-8007-19453449441c.png)

System Requirements :

OS : Ubuntu 20.0.04 LTS
CPU : Intel Core i3 and above.
RAM : 4 GB
Memory : 256 GB SSD.


References :
[1] https://www.youtube.com/watch?v=2Qu4LCvB4bs
[2] https://www.youtube.com/watch?v=iwciZDZ0OWM
