# ALX GraphQL Projects

This repository contains multiple GraphQL and React-based projects completed as part of the **ALX Frontend Specialization - GraphQuest: Exploring and Implementing GraphQL** module.  
The work explores fetching and displaying data from the [Rick and Morty GraphQL API](https://rickandmortyapi.com/graphql) using raw queries and React applications with Apollo Client.

---

## 📂 Repository Structure

alx-graphql-0x00/ # Basic GraphQL queries using .graphql files and cURL
└── character/
├── README.md
├── character-id-1.graphql
├── character-id-1-output.json
├── character-id-2.graphql
├── character-id-2-output.json
├── character-id-3.graphql
├── character-id-3-output.json
├── character-id-4.graphql
├── character-id-4-output.json
├── characters-page-1.graphql
├── characters-page-1-output.json
├── characters-page-2.graphql
├── characters-page-2-output.json
├── characters-page-3.graphql
├── characters-page-3-output.json
├── characters-page-4.graphql
├── characters-page-4-output.json
└── episode/
├── README.md
├── episode-id-1.graphql
├── episode-id-1-output.json
├── episode-id-2.graphql
├── episode-id-2-output.json
...

alx-graphql-0x01/ # Next.js + Apollo Client setup
└── alx-rick-and-morty-app/
├── graphql/apolloClient.ts
├── graphql/queries.ts
├── pages/_app.tsx
├── README.md

alx-graphql-0x02/ # Full React app querying episodes
└── alx-rick-and-morty-app/
├── components/common/EpisodeCard.tsx
├── interfaces/index.ts
├── pages/index.tsx
├── README.md



---

## 📜 Project Descriptions

### **0x00 - Basic GraphQL Queries**
This section contains GraphQL queries to fetch specific characters, paginated lists of characters, and specific episodes.

#### Tasks:
1. **Fetch a specific character by ID**
   - File: `character-id-{n}.graphql`
   - Output: `character-id-{n}-output.json`
   - Fields: `id`, `name`, `status`, `species`, `type`, `gender`

2. **Fetch a list of characters by page**
   - File: `characters-page-{n}.graphql`
   - Output: `characters-page-{n}-output.json`
   - Fields: `id`, `name`, `status`, `image`

3. **Fetch a specific episode by ID**
   - File: `episode-id-{n}.graphql`
   - Output: `episode-id-{n}-output.json`
   - Fields: `id`, `name`, `air_date`, `episode`

#### How to run:
Example for fetching character with ID 1:
```bash
curl -X POST https://rickandmortyapi.com/graphql \
-H "Content-Type: application/json" \
-d '{"query":"query { character(id: 1) { id name status species type gender } }"}' \
| jq '.' > character-id-1-output.json

npm install @apollo/client graphql
npm install @types/graphql

https://rickandmortyapi.com/graphql