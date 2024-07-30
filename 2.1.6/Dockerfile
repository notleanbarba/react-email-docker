FROM node:lts-alpine3.20

WORKDIR /react-email

RUN npm init
RUN npm install react-email@2.1.6 @react-email/components@0.0.22 -E
RUN mkdir emails

COPY package.json .

EXPOSE 3000

CMD npm run dev 
