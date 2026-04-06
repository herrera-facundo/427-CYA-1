# Project Prometheus — Zuno App

Project Prometheus, officially titled "Zuno", is a mobile application designed to revolutionize student learning by leveraging artificial intelligence to transform course materials and assignments into personalized study aids.

# **Project Prometheus**

## **Overview**

Zuno is an intelligent **AI-powered study aid app** designed to help students learn more efficiently.
The system leverages **machine learning and natural language processing (NLP)** to:

- Generate personalized study resources from course materials and lecture notes.
- Recommend study decks based on user progress, deadlines, and performance.
- Track learning over time and adapt to the user’s strengths and weaknesses.

The project consists of:

- A **React Native mobile frontend** (cross-platform for Android and iOS using Expo).
- A **FastAPI backend**.
- A **PostgreSQL database** for storing user data, study decks, and progress.
- **Gemini integration** to generate study materials dynamically.

---

## **Tech Stack**

| Layer                  | Technology                          |
| ---------------------- | ----------------------------------- |
| **Frontend (Mobile)**  | React Native (Expo)                 |
| **Backend (API)**      | FastAPI                             |
| **Database**           | PostgreSQL                          |
| **AI Services**        | Gemini API                          |
| **Version Control**    | Git + GitHub                        |
| **Deployment (Later)** | Render or local tunneling via Ngrok |

## **Setup Instructions**

### **1. Prerequisites**

Make sure you have the following installed on your system:

| Tool                                      | Required Version                                 |
| ----------------------------------------- | ------------------------------------------------ |
| [FastAPI](https://fastapi.tiangolo.com/)  | 0.121.2 or later                                 |
| [npm](https://www.npmjs.com/)             | 9.x or later                                     |
| [PostgreSQL](https://www.postgresql.org/) | 15 or later                                      |
| [Git](https://git-scm.com/)               | Latest                                           |
| [Expo CLI](https://docs.expo.dev/)        | Installed globally via `npm install -g expo-cli` |

---

### **2. Clone the Repository**

```bash
git clone https://github.com/herrera-facundo/Project-Prometheus.git
cd Project-Prometheus
```

---

### **3. Backend Setup**

**Location:** `code/backend`

1. Navigate to the backend folder:

   ```bash
   cd code/backend
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Create a `.env` file:

   ```bash
   touch .env
   ```

4. Start the backend:

   ```bash
   npm run dev
   ```

   > Your API should now be live at `http://localhost:5000`.

---

### **4. Frontend Setup**

**Location:** `code/frontend/zuno`

1. Navigate to the frontend folder:

```bash
cd .\code\frontend\zuno\
```

2. Download project packages (npm):

```bash
npm i
```

3. Create a `.env` file under the `zuno/` root folder with the following content:

```bash
EXPO_PUBLIC_API_URL=<your_ip_address>:8000
```

4. Start the dev server (Metro / Expo):

```bash
npm start
```

5. Launch App:

- **Android device/emulator**: with the dev server running press a in the terminal, or run:

```bash
npm run android
```

- **iOS device/emulator**: with the dev server running press i on the terminal, or run:

```bash
npm run ios
```

- **Physical device**: scan the QR code shown by Expo using the Expo Go app.

---

## **Running the Full Stack**

1. Open **two terminal windows**:

   - **Window 1 (Backend):**

     ```bash
     cd code/backend
     npm run dev
     ```

   - **Window 2 (Frontend):**

     ```bash
     cd code/frontend
     npx expo start
     ```

2. Verify everything works:

   - API is reachable at `http://localhost:5000/ping`.
   - Frontend shows the mock decks for now.

---

## **Team Roles and Responsibilities**

Facundo Herrera Rivarola: Team lead.
Jake van Halder: Frontend lead.
Ethan Knigge: Backend lead.
Josh Anthony Santiago: AI lead.

**Folders**

`code` _Contains the frontend and backend code for Zuno_

`docs` _The documents and videos produced during the development of Zuno_

`resources` _Resources used to aid in the development of Zuno_

`tests` _Code used to test Zuno_

**Current Progress**

`Sprint 1`:

- Clear Functional and Non-Functional Requirements
- Documentation of User Stories, Use Cases, and UML Diagrams
- Identified skills needed to learn and skills already learned
- Required Software Decided and Installed
- Created Kanban Board with completed and some future tasks listed
- Created basic demo of the application without AI integration yet

`Sprint 2`:

- AI quiz generation and file handling
- File upload for course materials
- Backend structure and architecture
- Working UI prototype based on high-fidelity wireframes
