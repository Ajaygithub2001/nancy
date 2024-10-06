Nano Participation System
This project is a simple Nano-based participation system where users can join by sending a fixed amount of Nano to an admin wallet. Once the required number of participants join, a random participant is selected as the winner, and all the funds collected are transferred to their wallet.

Features
Users connect their Nano wallet and participate by sending 0.02 Nano to the admin wallet.
The admin wallet collects all contributions.
Once 100 participants join, a random participant is selected as the winner using a simulated Chainlink Verifiable Random Function (VRF).
All collected funds are transferred to the selected winner.
Participants and winners are stored in a virtual file system:
Participants File: Stores the wallet addresses of all participants during a round.
Winners File: Stores the winners' wallet addresses for each completed round.
Participants' file is cleared after each winner announcement, and the winners' file is appended with each winner.
How it Works
User Flow:
Users enter their Nano wallet address and click Connect.
After connecting, users can click Join to send 0.02 Nano to the admin wallet.
Their wallet address is stored in the virtual file system and displayed in the participant log.
Once 100 participants have joined, the system randomly selects a winner using a simulated Chainlink VRF.
The winner is displayed, and the participant log is cleared for the next round.
The winner's wallet is added to the winners' log.
Admin Wallet
The admin wallet address is hardcoded as:

nano_3m1pir3qb3ciyxsupsmo3zf1t3f1yccx8pjokj97tk9ya4oq333h69utzu4f

This wallet collects the participation fees and distributes the total amount to the winner.

Virtual File System
The program uses a virtual file system to simulate file storage for participants and winners:

Participants File: Contains the wallet addresses of all current participants. This file is cleared once a winner is selected.
Winners File: Stores the wallet addresses of all past winners. This file persists across rounds.
Log Display
Participant Log: Displays the wallet addresses of all participants who have joined the current round.
Winners Log: Displays the wallet addresses of the winners from previous rounds.
How to Run
Clone or download the project.
Open the index.html file in any browser.
Enter a Nano wallet address to participate.
Technologies Used
HTML/CSS: For building the user interface.
JavaScript: For handling user interactions, connecting wallets, managing the virtual file system, and simulating the random participant selection process.
Chainlink VRF Simulation: A simulated random number generator mimicking Chainlink's VRF to ensure fairness in selecting a winner.
Notes
The program is currently a frontend simulation and does not include real wallet connections or fund transfers. In a real deployment, the Nano wallet integration would need to be set up to handle real transactions and randomness using Chainlink VRF.
The fee for participation is fixed at 0.02 Nano.
The project uses JavaScript to simulate sending Nano and selecting the random participant, but it does not process real blockchain transactions.
Future Improvements
Blockchain Integration: Implement real wallet connections using Nano RPC and integrate Chainlink VRF to securely and verifiably select a random participant.
Backend Storage: Replace the virtual file system with server-side storage for participants and winners.
Security Enhancements: Ensure that all transactions and wallet connections are secure by integrating real Nano wallet functionality.
