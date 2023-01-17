
Client:
```bash
cd client
npm install
npm start
```

Server:
```bash
cd server
docker-compose up --build
```



## Tech Stack

**Client:** React, TypeScript

**Server:** Go (Golang), Gin, Python, Celery, RabbitMQ, Docker, Socket.IO, DALL-E-2, GPT, MongoDB

## Inspiration 💡
Our inspiration for this project was to leverage new AI technologies such as text to image, text generation and natural language processing to enhance the education space. We wanted to harness the power of machine learning to inspire creativity and improve the way students learn and interact with educational content. We believe that these cutting-edge technologies have the potential to revolutionize education and make learning more engaging, interactive, and personalized.

## What it does 🎮
Our project is a text and image generation tool that uses machine learning to create stories from prompts given by the user. The user can input a prompt, and the tool will generate a story with corresponding text and images. The user can also specify certain attributes such as characters, settings, and emotions to influence the story's outcome. Additionally, the tool allows users to export the generated story as a downloadable book in the PDF format. The goal of this project is to make story-telling interactive and fun for users.

## How we built it 🔨
We built our project using a combination of front-end and back-end technologies. For the front-end, we used React which allows us to create interactive user interfaces. On the back-end side, we chose Go as our main programming language and used the Gin framework to handle concurrency and scalability. To handle the communication between the resource intensive back-end tasks we used a combination of RabbitMQ as the message broker and Celery as the work queue. These technologies allowed us to efficiently handle the flow of data and messages between the different components of our project.

To generate the text and images for the stories, we leveraged the power of OpenAI's DALL-E-2 and GPT-3 models. These models are state-of-the-art in their respective fields and allow us to generate high-quality text and images for our stories. To improve the performance of our system, we used MongoDB to cache images and prompts. This allows us to quickly retrieve data without having to re-process it every time it is requested. To minimize the load on the server, we used socket.io for real-time communication, it allow us to keep the HTTP connection open and once work queue is done processing data, it sends a notification to the React client.

## Challenges we ran into 🚩
One of the challenges we ran into during the development of this project was converting the generated text and images into a PDF format within the React front-end. There were several libraries available for this task, but many of them did not work well with the specific version of React we were using. Additionally, some of the libraries required additional configuration and setup, which added complexity to the project. We had to spend a significant amount of time researching and testing different solutions before we were able to find a library that worked well with our project and was easy to integrate into our codebase. This challenge highlighted the importance of thorough testing and research when working with new technologies and libraries.
