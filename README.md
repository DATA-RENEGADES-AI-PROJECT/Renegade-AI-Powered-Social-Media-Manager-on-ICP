# Renegade-AI-Powered-Social-Media-Manager-on-ICP
This project aims to build an AI-based social media manager and content generator on the Internet Computer (ICP) blockchain using OpenAI's API. The system will generate tweets, captions, and blog posts, store them on ICP, and manage automated posting to various social media platforms.


⚠️ After deployment, you’ll use the actual canister ID from your deployed network.

React frontend running served by ICP, not by a traditional Node.js server — it’s now decentralized!


npm install @dfinity/agent @dfinity/auth-client @dfinity/principal
Then in your React code (e.g., App.js), you can connect to the backend canister like this:

javascript
Copy code
import { HttpAgent, Actor } from "@dfinity/agent";
import { idlFactory, canisterId } from "../../declarations/my_icp_app_backend";

const agent = new HttpAgent();

const backend = Actor.createActor(idlFactory, {
  agent,
  canisterId,
});

async function getGreeting() {
  const result = await backend.greet("ICP User");
  console.log(result);
}



``javascript``
dfx start --background
dfx deploy
Then open your browser and visit:

👉 http://localhost:4943/

You’ll see your React frontend running served by ICP, not by a traditional Node.js server — it’s now decentralized!
``javascript``


``javascript``
Step 6 — Deploy to the main Internet Computer network

Once satisfied:

dfx deploy --network ic


This will:

Upload your backend canister code to the Internet Computer blockchain.

Upload your React build (as static assets) to the asset canister.

Give you a public URL like:

https://<your-frontend-canister-id>.icp0.io


That’s your fully decentralized web app — front-end and backend running on ICP.

``javascript``