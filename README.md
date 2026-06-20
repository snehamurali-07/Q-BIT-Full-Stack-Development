# Q-BIT — 2-Qubit Quantum Gate Visualizer & Simulator

Q-BIT is a sophisticated, full-stack educational web platform designed to bridge the gap between abstract quantum information theory and intuitive circuit engineering. By combining a reactive drag-and-drop user interface with a high-performance linear algebra simulation engine, the platform translates $4 \times 4$ unitary matrices into an interactive, visual narrative, allowing users to explore real-time quantum states, superposition, and entanglement.

---

## System Architecture & Tech Stack

The application utilizes a decoupled Client-Server architecture optimized for low-latency, real-time recalculations:

*   **Frontend (Presentation Layer):** Built with **React.js (via Vite)** for high-performance state management and dynamic UI updates. 
    *   *Layout & Styling:* **Tailwind CSS** implementing a custom, single-viewport "Dark Space" glassmorphic aesthetic to completely eliminate vertical scrolling.
    *   *Drag-and-Drop:* **@dnd-kit/core** for real-time tracking, sorting, and positioning of quantum gates onto parallel qubit wires.
    *   *API Client:* **Axios** managing non-blocking, asynchronous payload handshakes to the server.
*   **Backend (Application Layer):** Powered by **Java 25** and the **Spring Boot 4.0** framework, serving as the high-fidelity computational core.
    *   *Build & Dependency Management:* **Maven** managing dependencies (Lombok, MySQL Connector, etc.).
    *   *Boilerplate Reduction:* **Lombok** for clean entity and model parsing.
*   **Persistence Layer (Database):** **MySQL Server** ensuring robust, ACID-compliant session tracking and secure user workspace isolation via **Spring Data JPA / Hibernate** Object-Relational Mapping (ORM).

---

## Key Engineering Features

*   **Real-Time Unitary Transformation Engine:** Every visual interaction or qubit toggle on the frontend dispatches a highly structural JSON payload to the Spring Boot REST API. The custom Java backend maps gate sequences to mathematical representations ($2 \times 2$ matrices for single-qubit gates, $4 \times 4$ for interaction gates like CNOT and SWAP) and computes the evolving statevector in milliseconds.
*   **High-Precision Complex Number Library:** Developed a native `ComplexNumber` matrix-vector math engine in Java to execute Kronecker products and matrix calculus without loss of precision, ensuring the statevector rigorously adheres to quantum normalization constraints.
*   **Live Dirac Notation Formatting:** Eliminates academic barriers by automatically formatting raw, multidimensional statevector arrays into clean human-readable Dirac notation strings (e.g., $\frac{1}{\sqrt{2}}|00\rangle + \frac{1}{\sqrt{2}}|11\rangle$) directly inside the real-time results footer.
*   **Secure User Environment:** Implemented a unified authentication/registration portal with state persistence to provision secure, private user workspaces.

---

## Project Documentation & Showcase

> **Code Privacy Notice:** The underlying source code for this project is hosted in a private repository to protect academic integrity and core simulation assets. Complete structural breakdowns, design schemas, or code segments are fully available for review upon request during technical interviews.

*   **Detailed Technical Report:** Review the comprehensive architecture design, backend process flows, and database structures in the Q-BIT Documentation.pdf.
*   **Visual Interface Gallery:** Explore the complete interface, including user registration modules, active database entries, and live quantum state results within the `Screenshots/` folder.

---

## Core Engineering Skills Applied

*   **Full-Stack Web Systems:** Component-driven state machines, decoupled system communication, asynchronous RESTful API design.
*   **Database Administration:** Relational database schema validation, data type enforcement, ORM bridging, and transaction safety.
*   **Scientific Computing:** Algorithmic translation of linear algebra, matrix calculus, and complex number arithmetic into scalable Java runtime logic.
*   **UI/UX Design:** User-centric workflows, absolute viewport budgeting, and responsive data synchronization.
