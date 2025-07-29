# Serverless Blog App with AWS Lambda

## Overview

The Serverless Blog Application is a modern, lightweight web app designed to allow users to create, view, and delete blog posts without relying on a traditional server-based backend. This project leverages the serverless architecture model, using various AWS services to ensure high scalability, low maintenance, and cost efficiency. By going serverless, the application handles dynamic backend tasks like data storage and processing without ever needing to provision or manage servers.


## Frontend Architecture
At the core of this application lies a static frontend interface built using HTML, CSS, and JavaScript (with jQuery for simplicity). This frontend is hosted on Amazon S3, which serves the static files (like index.html, scripts.js, styles.css, and images) as a public website. The UI provides users with a clean and responsive experience for interacting with blog content, including a modal form to add posts and live updates of post lists.

##  API Integration with AWS Gateway
All blog data is stored in Amazon DynamoDB, a fully managed NoSQL database service. A single table named BlogPosts is used, where each post is uniquely identified using a postId (a numeric key), and associated with a title, content, and optional URL. Lambda functions are granted permission to interact with this table through IAM roles, which follow the principle of least privilege to ensure secure access.

By using a combination of API Gateway, Lambda, and DynamoDB, the application runs entirely without traditional servers. It automatically scales to handle incoming requests, and the pay-per-use model ensures cost-effectiveness—billing occurs only when actual usage happens. Additionally, since S3 handles static hosting and Lambda handles all backend logic, the system remains highly maintainable and easily extendable.


## AWS Lambda Functions
Covers the three Python-based Lambda functions and their responsibilities:
CreateBlogPost.py
GetAllBlogPost.py
DeleteBlogPost.py

## Conclusion

This project demonstrates the practical application of a fully serverless architecture on AWS. It combines static frontend hosting with dynamic, on-demand backend processing and storage. The result is a clean, efficient, and production-ready blog platform that is ideal for learning serverless patterns, building personal projects, or laying the groundwork for more complex serverless applications in the future.
