FROM  node

WORKDIR /app

COPY package.json .

RUN  npm install

COPY . .


RUN npm run build


ARG DEFAULT_PORT=3000
ARG DEFAULT_API_PORT=8000

ENV PORT=$DEFAULT_PORT

ENV API_PORT=${DEFAULT_API_PORT}

ENV API_URL=http://goal-backend:${API_PORT}

EXPOSE $PORT

CMD [ "npm" , "start" ]
