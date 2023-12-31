# Report 16- Week of 12/14/2023
Guess where we are? We are at Wakiki Beach in Hawaii!
After the final showcase, we summarized all the processes and details of the project and produced our summary report (PDF)

## Refining Project 2 
We are still working to make our Project 2 better! 
![weekly report](weekly-reports/手绘.png)


# Report 15- Week of 12/07/2023
Towards the end of the project, weilong gao and I combined our two production parts, and now we have our smart voice assistant, Chameleon Assistant!
Please watch our video! https://www.youtube.com/watch?v=zMBSnCiyt1o
![weekly report](weekly-reports/95.jpg)
![weekly report](weekly-reports/91.jpg)

## Refined Project Description 
Hi there
We are Weilong and Yang. We strongly believe that when it comes to assistants, like Siri and Alexa, different users have different needs. That's why we envision a future where these assistants become more user centric. For instance some users may prefer a strong assistant that helps them manage tasks while others may appreciate a companion who keeps them on track with responsibilities.
To turn this vision into reality we've created the Chameleon Assistant. It's an assistant with character traits that can cater to voices and preferences. It is also connected to our table robot built based on particle platform, and showing different motions based on our interaction.

## Design Different Movement 4 Our Table Robot
As mentioned earlier, our table robot will take different actions according to different conversation states. For example, when you speak to the chameleon assistant, the table robot will make a thinking expression "o_O" and slowly nod up and down. When the Chameleon Assistant replies, the table robot will dance happily in front of you! But when there is no command, it will display the current time in SF time zone.
![weekly report](weekly-reports/99.jpg)
![weekly report](weekly-reports/92.jpg)
Here is a real conversation scenario:
Ah, greetings! I am Chameleon Assistant, here to assist and accompany you on your quest for knowledge and assistance. My purpose is to adapt to your desires and adopt a character that suits your preferences. So, dear interlocutor, which character would you prefer I adopt? (Table Robot Dancing)
Could you please be a rap star? (Table Robot Thinking)
Yo, yo, yo! What's poppin', my friend? They call me MC Chameleon, the rhyme-spittin' rap star assistant ready to drop some lyrical knowledge. So, tell me, what's on your mind? How can I assist you in the world of beats and rhymes today?(Table Robot Dancing)

Please remind me in 10 seconds that I need to go to take a shower. (Table Robot Thinking)
Yo, time's tickin'! In just 10 seconds, you gotta hit the shower, my friend. No time to waste, no excuses to linger. Get yourself clean, stay fresh and crisp. The countdown starts now, so make a move and get the water drippin'. Peace out! 10... 9... 8... 7... 6... 5... 4... 3... 2... 1... Shower time! (While waiting, Table Robot in Standing By Mode)
![weekly report](weekly-reports/100.jpg)

## Final Showcase Feedback
Two frequently asked questions are:
1. With the support of Open AI, our chameleon assistant can become anyone the customer wants, but this will also raise concerns about ethics. Will our chameleon assistant become a racist? I think at present In this case, it will not be possible, because our model is built based on the gpt api provided by Open AI. Open AI has very strict ethical restrictions on gpt internally, but I noticed an llm called alpaca, developed by Stanford University. . Alpaca is an offline large oracle model, which means that people can maliciously tamper with the model's data set, which raises concerns about AI ethics.
2. Another suggestion that is often raised is whether we can change the movements and expressions of our robot to suit the character of our choice (such as a history professor, a policeman, or a rapper)? The answer is yes, we can let gpt make the robot react differently based on the emotional value of the selected character. (For example, set the mood value from 1 to 10, with 1 being the least happy and 10 being the happiest. We set the mood index of a history professor who comes home from work to be 3, because she may be very tired after a day of work) With the existing LLM, we can ask ChatGPT to draw inferences and design different expressions and actions for us to correspond to different emotional values.
3. At the end of our showcase, Dr. Kosa gave a short feedback: This year, 7 out of 8 groups are using LLM. I believe this number was 2 last year, and 0 two years ago. We can clearly see the trend of how AI are changing our design thinking. I beleive it is a really interesting point, will AI be the major trend for future design? 

## Speculation 
To human experience: The unexpected speed of AI development makes the "digital bespoke era" possible. We believe, in the near future, everything, such as mobile APPs, Smart furniture, will all become bespoke for each individual. Regarding engineering, it does show the hint that a table robot can unconsciously enhance people's sense of time management and boost work efficiency. We think the movement of our table robot can also be fully customized, depending on the user's mood.

## Project Conclusion
In conclusion, we have explored how to use ChatGPT to self program, and how to connect LLM with a physical model through a microcontroller. We believe this will greatly promote our future works.
![weekly report](weekly-reports/87.jpg)
![weekly report](weekly-reports/88.jpg)
![weekly report](weekly-reports/89.jpg)


# Report 14- Week of 11/30/2023
In this project, I will be responsible for the production of 3D models, the design and assembly of Microcontroller and programming on Particle IDE (including the design of the robot's movements, each movement corresponds to a different number), Weilong Gao will be responsible for the AI voice For the assistant part (including calling APIs, training models, etc.), and sending digital instructions to Photon 2, we will be responsible for completing the video production, and Weilong Gao will be responsible for the pdf production.

## Model Making 
Based on the 3D model I designed on Rhino last week, I drew a 2D drawing on Adobe AI and chose to use laser cutter to create the physical model. Thanks to Project 1, I can now control the laser cutter perfectly. I used 1/8 in and 1/16 in thick clear acrylic sheets. I was surprised to find that the hard transparent acrylic sheets can also become "soft" after being engraved with a fine laser cutter!
The reasons why I don’t use 3D printing are:
1. I want a transparent model to help users see the internal mechanical structure
2. The models printed by Jacobs Maker Space’s 3D printer are not refined enough.
3. 3D printing will be very time-consuming, which is not friendly to us who need to constantly modify the model.
![weekly report](weekly-reports/81.jpg)
![weekly report](weekly-reports/90.jpg)

## Test on Arduino Nano
Even though I finally decided to use the Particle Photon 2, I used an Arduino Nano during the initial testing phase because the Arduino Nano and Photon 2 are very similar to some extent. I used two SG90 9G servos, and a small OLED screen. During the experiment, I found that two SG90 servos require a voltage of 5v to support operation, but the particle photon 2 can only provide a voltage of 3.3v, so I purchased an additional power supply from Jacobs material store, four AA batteries. But the OLED screen is still connected to the 3.3v. In tests using Arduino Nano I had success, both servos and OLED worked fine under my instructions
![weekly report](weekly-reports/84.jpg)
![weekly report](weekly-reports/85.jpg)
![weekly report](weekly-reports/86.jpg)

## Switch to Particle Photon 2
Because our robot ultimately needs to be connected to our AI model through the network, photon 2 is the microcontroller we finally decided to use. In terms of connection, photon 2 and Arduino nano are very similar, but I still made some changes in the connection based on the design drawings of photon 2. In the code part, I found that although the underlying logic of the arduino code and the photon code are the same, a lot of modifications are still needed. With the help of Zoey, I successfully found the corresponding library. I think the advantages of photon 2 compared to arduino are:
1. Can be connected to the Internet, which allows us to use photon 2 to make real IoT designs
2. Particle IDE is better designed than Aruino IDE
3. Stronger computing power
![weekly report](weekly-reports/96.jpg)
![weekly report](weekly-reports/93.jpg)

## Combining Model with Microcontroller 
Now it is time to connect two parts together! I installed the servo and OLED screen in the preset slots on the model. The assembled model is still very delicate. The transparent model allows us to see the inside of the model! Because it was my mother’s birthday that day, I displayed Happy Birthday Mom on the OLED screen. My mother was very happy when she saw it.
![weekly report](weekly-reports/101.jpg)
![weekly report](weekly-reports/97.jpg)


# Report 13- Week of 11/23/2023 Thanksgiving Week
I changed my design direction. After applying to TJ and Jeff, I chose to work with Weilong Gao. We had a new topic, a desktop AI voice assistant robot. The project will consist of two parts: an AI voice assistant, and a desktop robot

## AI Voice Assistant 
Traditional voice assistants, such as Siri or Alexa, answer questions for customers under a preset situation. However, different customers have different needs. Can we allow customers to set up their voice assistants? What about the personality they want? For example, a strict teacher, or a caring friend? We also noticed that when using ChatGPT, we must first start a conversation with chatgpt before it can respond to our questions. Is there a way for our AI model to start a conversation first?

## Table Robot
We want to use the fewest parts to achieve the most movements. I made a simple 3D model using Rhino and started to imagine the parts of our microcontroller.
![weekly report](weekly-reports/83.jpg)
![weekly report](weekly-reports/82.jpg)
## Summary
Most of our progress this week stayed at the idea level, because it was Thanksgiving, and I went to New York to spend a perfect Thanksgiving with my friends.



# Report 12- Week of 11/16/2023

## Toward Project 4
Now it is time to use what I have learned from the past 3 projects to create a new project 
Project 4 summary: A while back, a friend of mine who lives in downtown Berkeley was burglarized. The University of California, Berkeley is known as one of the most dangerous universities in the United States, with countless criminal incidents occur every day. I want to design a security gate to protect private property. I believe this will be a great opportunity for me to practice skills that I have learned from TDF class. I will consider using grasshopper to make the physical model of my door lock, and then I will use API and Particle system for face recognition and door lock control system.
![weekly report](weekly-reports/Snipaste_2023-11-16_14-22-00.jpg)
## Research Plan 
1. Grasshopper Modeling：I will combine what I learned from project 1 and design the system of my physical model. Using Grasshopper allows me to make small edits to my model at the end.
2. AI Technology：I have started my research on Facial Recognition APIs from Baidu AI platform, I am also thinking of using LLM as the vocal assistant.
3. Particle System：I will explore how to use Particle system to control the door lock. More importantly, I want to study how it works together with different AI techs.
4. Design Analysis：Empathy will be the core idea of this project, because I want to solve the actual problem by my design.

## Current Work 
In present, I have completed the market research, interviewed the friends who suffered the burglary incident, and made a complete user flow. I also began to learn the face recognition API in Baidu AI



# Report 11- Week of 11/09/2023

## LLM Project Finished
I added 7 complete chunks of information, which includes my previous Project descriptions on My Portfolio Website and of course our weekly report
![5](weekly-reports/i5.jpg)
## Study of similarity threshold
A higher similarity threshold means that the information I input will be more similar to the gpt's answer, which I want to avoid. I want people who ask questions using my mini me to get more diverse responses than just what I type in information chunks.

## Result of Question 1 
It mentioned Grasshopper, Photon, and AI
![1](weekly-reports/i1.jpg)
## Result of Question 2
It picked Pufferfish, which is the Photon Project. Based on the information I had on weekly report, it pointed that our product is currently single-use product that cost 90 dollars, and it encouraged me to think about the reusability
![2](weekly-reports/i2.jpg)
## Result of Question 3
I added a bunch of other ocean related projects, but I only input the project descriptions in each chunk, so it ended up picking pufferfish again since pufferfish projects has the longest text
![3](weekly-reports/i3.jpg)
## Result of Question 4
Since in the background setting, I am the emperor, so it returned a bunch of compliments
![4](weekly-reports/week 5 report/i4.jpg)

## Challenges
For this project I chose 01-Triceratops. First of all, it was a very interesting project, and I enjoyed the process of optimizing the model. However, I also consider that this is my first formal project editing LLM, and I hope to preliminatively understand the Fine-Tuning process through this project, such as learning the impact of similarity threshold and token length on the result, so I choose level 1- Triceratops. I completed a series of experiments with ZeroWidth following the steps and video tutorials given in the bcourse to understand the impact of ZeroWidth instructions and information on Fine-Tuning, but after I completed the training I realized that Project 2 - Puffer Fish Rescuer has the longest text description among all the information chunks, far longer than other projects, which also led to the fact that when I was asked about my past projects, GPT knew more about Project 2 than other projects, and always selected Project 2 as an example. To solve this problem I added more information to other projects, for example, I added some textual descriptions of the research process from previous portfolios to my database.

## Speculations 
I think ZeroWidth can greatly simplify the college admissions process. For example, if a student wants to apply for Master of Design programs in multiple schools, like UCB, Harvard, and CMU, he only needs to create his Mini Me on ZeroWidth, add his portfolio and CV and other personal information to the database, and choose the more High similarity threshold. Then admissions officers from different schools can get to know the student more objectively just by asking Mini Me. Because my roommate is a mechanical engineering student at UC Berkeley, I discussed with him about the applications and prospects of ZeroWidth and other LLMs in the engineering field. His answer surprised me- Almost all mechanical engineers are learning AI, because it is disruptive to the field of mechanical engineering, and AI is more flexible and efficient. Taking ZeroWidth as an example, it can greatly reduce the workload of mechanical engineers. When testing the feasibility of a project, engineers can feed all the data to ZeroWidth and ask a series of questions. If it is on GPT, they will have to feed the data everytime they started a conversation.

## Next Step
NEXT STEP, I will explore the possibility of ZeroWidth deeper. Because I think ZeroWidth invents a new and unique way to learn about a person. I can't wait to see ZeroWidth build cooperation with Linkedin. 
I also hope to gradually improve my Mini Me and add more information about myself as a designer to my database. Maybe one day I can use my Mini Me to replace the Zoom interview. GPT has very advanced image recognition capability based on its powerful model structure and database, so I am thinking whether I can add some pictures of my works to my ZeroWidth database? The images of the design may have more impact than the words


# Report 10- Week of 11/02/2023

## Large Language Model
This week we started our third project-Mini Me, by using ZeroWidth, a LLM build based on gpt 4.0 
I beleive it will be a new advanture for me. I am familiar with GPT but I am not really familiar with fine turning. So lets see
![6](weekly-reports/i6.jpg)
## Hand On Practices
I have started working on the model. Created my account on ZeroWidth and follow the instruction on the model. By inputting some instructional information about me (Yang Cen), such as my designer’s weekly report and introduction of past works, others can ask some questions about my works through ZeroWidth. I think it is a very good platform based on gpt 4.0, which helped me get familiar with LLM training.

## Questions Prepared For My Model 
First, to get a direction for my practice on LLM, I have listed four questions that others might ask my Mini Me, all about projects I have worked on:
1.In one sentence, can you talk about my interest fields of design?
2.Picking one of my previous project and give advices for it.
3.Based on my previous projects, what do you think about the future product design for our ocean.
4.Overall, evaluate my story telling skills for my previous projects



# Report 9- Week of 10/25/2023

## Previous projects
Now I have finished two projects so far. In my first project, it is a personal project, I used Grasshopper to design a phone stand for foldable phone users, which is also my first time using Grasshopper, excited but also complicated. Grasshopper enabled me to create designs and customize the stand to meet the requirements of different phone users. Then in the second project, it was an team effort, where we developed a life vest called "pufferfish” for free divers by utilizing the photon 2 platform. In both projects, I have experienced using some interesting tools and learned from them

## Speculation for the third project
As we transition to our third project involving AI applications, I'm eager to explore and integrate the various APIs I've previously encountered. I believe harnessing the power of AI can introduce innovative solutions and redefine the way we approach design challenges in the realm of emerging technologies.

# Report 8 - Week of 10/18/2023
Last week before the final presentation! All team members gathered together and we are filming and editing our presentation video, we want audience to have fun
![Pufferfish](weekly-reports/16.jpg)
## Final Product Test

Weilong and Yani debugged our product this week, thanks to their contribution. It is a product ready to go. The monitor will sense the heart rate of the diver, once he/she has a heart rate 20 times per min below his/her average heart rate. The device will vibrate and notify the diver. If the diver does not make a response within 5 seconds, which means that the diver might encountered a BO-Blackout, the life vest will be inflated and bring the diver back to the water surface. I think the idea of giving notification through vibration is a good idea, cause it can reduce the chance of error warning.

![Pufferfish](weekly-reports/8.png)

## Video Editing

Product video is always a lot of fun. Started with filming process, I wear the life vest and inflated it! It will definately bring my head to the surface of the water because it is really tight and almost chocked me. And more importantly it is one time use, yes! 90 dollar for just single use! That is why I said it is a really expensive project. Carina and I edit the video and combine different clips together. 
![Pufferfish](weekly-reports/11.jpg)
![Pufferfish](weekly-reports/12.jpg)
![Pufferfish](weekly-reports/13.jpg)
## My Contribute to the team and self-reflection
During the ideation phase, I believe my deep understanding of marine dynamics offered a lot of help in shaping the theme of our pufferfish rescuer project, especially in researching the challenges that free divers are facing and what similar product designers have created on the market. Although I am unfamiliar with the Photon microcontroller, I collaborated with my talented teammates, successfully integrating my marine expertise with their technical skills to enhance the functionality and responsiveness of our pufferfish rescuer. Last but not least, I took the responsibility of the video editing and shooting processes.
During the ideation phase, I believe my deep understanding of marine dynamics offered a lot of help in shaping the theme of our pufferfish rescuer project, especially in researching the challenges that free divers are facing and what similar product designers have created on the market. Although I am unfamiliar with the Photon microcontroller, I collaborated with my talented teammates, successfully integrating my marine expertise with their technical skills to enhance the functionality and responsiveness of our pufferfish rescuer. Last but not least, I took the responsibility of the video editing and shooting processes.
![Pufferfish](weekly-reports/14.jpg)
![Pufferfish](weekly-reports/15.jpg)

## Speculations 
### Human Experience 
The introduction of our pufferfish rescue vest will bring revolution to the diving community, because we switches free diving from an exciting yet risky “adventure”, into a absolutely save exploration of the underwater world. It's not just a rescue vest, but a safety promise to both beginners and advanced free divers. Now they can push their limits and explore deeper waters, because they know the fact- water will no longer take free divers’ lives. Pufferfish rescuer encourages those who were previously deterred by risks, who were scared of danger and potential accidents, to join free diving. This potentially leading to the expansion of free diving community, bring benefits to training schools and enthusiastic dive groups (more people to join). For family and friends who are worried on the shore, Pufferfish brings peace of mind alleviating their anxieties while waiting for the diver to resurface. While diving immerses you in nature’s rhythm, our amazing pufferfish rescuer ensures that the dance in the water continues!
### Mechanical Engineering 
The invention of our pufferfish rescuer means the coming of a new era in marine sports engineering advancements. A primary challenge is developing a heart rate monitor that's accurate under marine-environment. It should prevent false inflations while detecting heart rate anomalies. That is why we have the vibration warning system on pufferfish, you will have 5 seconds to react before false inflations. And the inflation mechanism, is well-known as one of the safest mechanism on the earth, since people are using that on the airplane. The material must be durable, yet flexible, to handle underwater pressures and ensure diver mobility. Ergonomic, a word that has been broadly discussed for free divers. Our pufferfish rescuer should be user-centered, which mean that it should accommodate various diver sizes and potentially customized requirements based on conditions or user needs. As the vest gains popularity and diving evolves, engineers must continually enhance its design to maintain safety standards.
### AI Tech
We believe machine learning can bring great contribution into the system of Pufferfish, it would enhance its safety features. By utilizing real time data analysis, like how an Apple Watch works, Pufferfish could proactively identify issues by comparing a divers vital signs with a huge amount of diving related data. This data would be stored offline and could potentially detect blackouts. The machine learning model would continuously learn from each dive gaining insights into user patterns and minimizing mistakes. If we also incorporated sensors that measure depth, pressure and temperature (I've actually experimented with this in one of my projects although it wasn't as accurate as the one) the AI system would provide a comprehensive overview of a divers physical condition. In case of emergencies the Pufferfish system could send real time distress signals along, with data to aid in rescues (including GPS information). After each dive Puffer AI would review your diving data, and provide analysis and updates. Pufferfish is a diving mentor enriching your diving experience.
![Pufferfish](weekly-reports/24.jpg)
![Pufferfish](weekly-reports/25.jpg)
![Pufferfish](weekly-reports/26.jpg)
![Pufferfish](weekly-reports/27.jpg)
# Report 7 - Week of 10/11/2023

## Connecting 2 photons

We had trouble connecting 2 photon devices, so we asked someone for help, and it eventually works. In case of our project, I think it will be easier to use ardduino since it does not really need to connect with the internet. 
![Pufferfish](weekly-reports/17.jpg)
![Pufferfish](weekly-reports/18.jpg)
## Get our hands dirty! 

Now we have a developed idea and we should move forward to design. The idea is to have a photo-centered system connected with an inflatable life vest. When the heartbeat monitor detects the diver's heartbeat is 20 times per minute below average, it will send a notification to the diver. If the diver does not turn off the notification in 5 seconds, the life vest will be inflated. Eventually, help the diver to resurface. 
![Pufferfish](weekly-reports/19.jpg)
![Pufferfish](weekly-reports/20.jpg)
![Pufferfish](weekly-reports/21.jpg)
![Pufferfish](weekly-reports/22.jpg)
## Selecting inflatable life vest on the market

We have found some well developed inflatable life vest on amazon, they are expensive but we got them! 

## We have also met some problem

The monitor we bought can only accept 5v but the export voltage of a photon 2 is only 2.2v, Weilong is really helpful and he solved the problem.  


# Report 6 - Week of 10/04/2023

## Ideation and New Team! 

This week, luckily, I got my new team and we are friend with each other. We started ideation and finally zoomed into one interesting topic- free diving. I love marine environment that is why we choose the idea. Instead of designing something for user group that we are not familiar with, we want to focus on something we know and make possitive changes to their lives. 

## So, what is the problem? 

Free diving, has one of the highest death rates among other marine sports. There are 10000 free divers in the United States, and every year, 20 free divers who have lost their lives, which is 1/500 of the free diving community. BO, which stands for Black Out, is the No.1 cause of death for Free Divers. Among 400 cases of BO accidents, 75% of divers lost their lives. When you encounter a BO, your teammate must rescue you immediately, or it might lead to irreversible damage, or death. You cannot self-rescue.

## How to solve the problem? 

We have studied from Avalanche Backpacks, which is a backpack skiier use when they encounter a avalanche. The airbag inside the bag will be inflated and help the user to flow on the surface of the snow. Maybe we can study from it? 


# Report 5 - Week of 09/27/2023

## Testing out Photon 2 at Home

This week we did some simple demos, it wasn't difficult, but it was a lot of fun, I used phaton 2 to make a simple flashing light. Since I have some experience with arduino, so I had a lot of fun discussion this with my friends on class. I have also been to the MDes website to check out previous student works, they are amazing! and I wish to make something cool like them
![IOT SetUp1](weekly-reports/微信图片_20230927020229.jpg)
![IOT SetUp2](weekly-reports/微信图片_20230927020232.jpg)

## Team Topics
I also chose the theme of the future group, and I think it is challenging to carry out complex product functions through modules. I am looking forward to the future group cooperation!


# Report 4 - Week of 09/20/2023

## Setting Up Photon 2 at Home

I finally had a short break after the project 1. This week's work was very easy. I set up my Photon 2 at home. Thanks to my previous experience with Arduino, I didn't find this setup to be a challenge. Even though I am familiar with such setups, I still chose to follow some tutorials to make this project more enjoyable! I have not yet completed the final step, which involves connecting to the school's IOT network. However, I plan to finish this before the upcoming class.
![IOT SetUp1](weekly-reports/微信图片_20230920135022.jpg)
![IOT SetUp2](weekly-reports/微信图片_20230920134941.png)

## Reflecting on the Importance of IOT Skills

I believe that mastering IOT is essential for industrial designers. Leveraging these small components allows us to implement a wide range of product functionalities, even if they may not always be perfect or flexible.



# Report 3- Week of 09/14/2023

## Design Concept Completion

This week, I completed the design concept, which was presented by hand drawing.
![Drwaing](weekly-reports/微信图片_20230913223723.jpg)

## Modeling with Grasshopper and Rhino

I also completed modeling with Grasshopper and Rhino. Then, I used a laser cutter to cut out different panels on a large piece of acrylic board.
![Grasshopper 1](weekly-reports/grasshopper.png)
![Model 1](weekly-reports/微信图片_20230914002350.jpg)
![Model 2](weekly-reports/微信图片_20230914002337.jpg)
![Grasshopper 2](weekly-reports/Snipaste_2023-09-14_00-21-04.png)

## Video Demonstration on YouTube

I also created a video demonstration and uploaded it on YouTube. The link is as followed: [Watch the Video](https://youtu.be/hNxhHeBuomM)



# Report 2 - Week of 09/07/2023 #

## Summary of the week

In the past one week (including an excited three-day weekend), I completed the 3D printing training online, and learned about Grasshopper tutorial by watching Youtube videos. This gave me a better understanding of Grasshopper, even though I still can't quite accept it as my main tool when designing. 

## Demonstration of the Ideal Phone Stand (My Rhino crashed when I tried to apply the grid texture onto its surface so I do not have a model yet)

Also this week, I sketched an ideal phone stand. I hope there is a phone stand that can support a foldable phone in two different folded states. I used Rhino to do some simple demonstrations.I'm a model enthusiast for warships, and I took inspiration from a photo-etched structure I recently assembled.
![Demonstration of the Ideal Phone Stand](weekly-reports/微信图片_20230906150917.jpg)
![Inspiration](weekly-reports/微信图片_20230906150914.jpg)

## Learning Challenges with Grasshopper

In the process of learning Grasshopper, I still have no way to fully understand the relationship between different batteries. At the current stage, Rhino and Fusion 360 are still my main tools for modeling.Maybe these tools are more useful for products without complex structures. However, I think what I learned in Grasshopper, such as the texture or grid of the surface of the object, will help me build more diverse products in the future.
![Grasshopper 1](weekly-reports/1.png)
![Grasshopper 2](weekly-reports/2.png)
![Grasshopper 3](weekly-reports/3.png)
![Grasshopper 4](weekly-reports/Snipaste_2023-09-06_14-59-14.png)
![Grasshopper 5](weekly-reports/WeChat_20230906170417.mp4)



# Report 1 - Week of 08/21/2023 #

## Learning State and Excitement about the Project

This week I gradually started to enter the state of learning. I was very excited when I heard that we can design a stand for a specific mobile phone, because I have a different mobile phone—Xiaomi Mix Fold 3.

### The Two States of Folding Phones

The folding screen mobile phone has two states, open and folded. I took measurements on my phone, which will help me in the later design. I predict that this mobile phone stand should be able to support two types of mobile phones at the same time.

### Market Trends

More and more folding screen mobile phones have appeared on the market. Perhaps this mobile phone stand will bring convenience to people.
![Demonstration of my phone](weekly-reports/微信图片_20230828145426.png)

## Laser Cutter Experience

At the same time, I also tried to use a laser cutter to cut the model of the mobile phone holder on the wooden board. It was not a perfect attempt, because the laser cutting machine did not completely cut the wood due to the adjustment of the parameters.

### Lessons Learned

So, I had to use a utility knife to remove and polish the wood, but I think it was a good lesson.
![Phone stand](weekly-reports/微信图片_20230829022141.jpg)




