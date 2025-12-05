# Brain Buzz

## Description

**Quiz Brain Buzz** is a fun and interactive quiz API built with **TypeScript** and **Express**. It allows users to manage quiz data (questions, answers, and participants) and supports both **local persistence** and **cloud storage** via Upstash KV. The project is designed for deployment on **Vercel** and integrates seamlessly with **GitHub**.

---

## Features

* Add, view, and clear quiz participants
* Echo endpoint for testing
* Persistent storage with **local JSON file**
* Cloud KV storage using **Upstash**
* Error handling and logging
* Fully deployable on **Vercel**
* Unit tests for backend functionality

---

## Installation

1. Clone the repository:

```bash
git clone <repository-url>
cd quiz-brain-buzz
```

2. Install dependencies:

```bash
npm install
```

3. Compile TypeScript (if not using ts-node):

```bash
npx tsc
```

4. Run the server locally:

```bash
npm start
# or with ts-node
npx ts-node src/server.ts
```

---

## API Endpoints

| Endpoint      | Method | Description                                           |
| ------------- | ------ | ----------------------------------------------------- |
| `/`           | GET    | Root URL, returns a welcome message                   |
| `/echo/echo`  | GET    | Echoes a query message                                |
| `/add/name`   | POST   | Add a new participant `{ "name": "YourName" }`        |
| `/view/names` | GET    | View all participants                                 |
| `/clear`      | DELETE | Remove all participants                               |
| `/data`       | GET    | Fetch all participants from Upstash KV                |
| `/data`       | PUT    | Update participants in Upstash KV `{ "data": [...] }` |

---

## Deployment (Vercel)

The **assets/** folder contains screenshots showing how to:

1. Connect GitHub repo
2. Create Vercel project
3. Configure environment variables (`KV_REST_API_URL` & `KV_REST_API_TOKEN`)
4. Deploy server and verify functionality

---

## Testing

Run unit tests with Jest:

```bash
npm test
```

---

## Environment Variables

* `PORT` – Server port (default from `config.json`)
* `url` – Base URL
* `DATABASE_FILE` – Local JSON file path
* `KV_REST_API_URL` & `KV_REST_API_TOKEN` – Upstash KV credentials

---

## Author

Dhruv S.

---
