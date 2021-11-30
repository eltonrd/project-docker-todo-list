FROM mjgargani/puppeteer:trybe1.0
WORKDIR /docker/todo-app/tests
COPY node_modules.tar.gz ./
COPY package.json ./
RUN npm install
COPY . .
EXPOSE 3001
CMD ["npm", "test"]
