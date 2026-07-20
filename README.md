# Music Library Micro Frontend

This project is the **Music Library Micro Frontend** used by the Host Application. It is independently deployable and exposed through Vite Module Federation.

---

## Tech Stack

* React
* Vite
* React Query
* React Hook Form
* Tailwind CSS
* MSW
* Vite Module Federation

---

## Features

* Fetch songs from iTunes Search API
* React Query custom hooks
* Loading and Error UI
* Filter songs
* Sort songs
* Group songs
* Add songs using mocked API
* Delete songs
* Admin/User role support

---

## Running Locally

### Clone Repository

```bash
git clone https://github.com/your-username/music-library.git

cd music-library
```

### Install Dependencies

```bash
npm install
```

### Run Development Server

```bash
npm run dev
```

Application runs on:

```
http://localhost:5001
```

---

## Connecting with Host

The Host Application should contain the following environment variable.

```env
VITE_MFE_REMOTE_URL=http://localhost:5001
```

The Host dynamically imports this Micro Frontend using Module Federation.

---

## Deployment

Live Demo

```
https://bespoke-cannoli-e755bd.netlify.app/
```

---

## Data Source

### Read Operations

Songs are fetched from the public iTunes Search API using React Query.

### Write Operations

Song creation and deletion are handled through mocked asynchronous endpoints implemented with MSW.

---

## React Query

The application uses custom hooks instead of calling `useQuery()` directly inside components.

Example:

```
useSongsQuery()
```

Mutations are handled using `useMutation()` with cache invalidation after successful operations.

---

## Project Structure

```text
music-library/
│── src/
│── public/
│── hooks/
│── components/
│── services/
│── vite.config.js
│── package.json
```

---

## Future Improvements

* Persistent backend storage
* Better caching strategy
* Search suggestions
* Pagination
* Performance optimization
* Unit testing
* End-to-end testing
