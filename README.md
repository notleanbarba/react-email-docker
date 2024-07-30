# Docker Image for React Email 

This a community repository of the [React Email Docker image](https://hub.docker.com/r/notleanbarba/react-email).

Run React Email development server without installing it on your local machine or in your project repo. Easily start an instance using Docker compose and auto refresh your email templates directly in your project repository.

## Use

Run this command for a single instance of React Email.

    docker run -p 3000:3000 -v path/to/emails/dir:/react-email/emails notleanbarba/react-email:latest

However, the best way to use the container is with docker compose. [^1]

    react-email:
      image: notleanbarba/react-email
      volumes:
        - path/to/emails/dir:/react-email/emails
      ports:
        - 3000:3000 

Mount a volume in container's directory `/react-email/emails` to render your email templates dynamically.

Open [localhost:3000](http://localhost:3000) (Or any port you used) and enjoy! 🥳

[^1]: Note: If you have a server running on port 3000 you can change the host port to any value (Example: 3001:3000).
