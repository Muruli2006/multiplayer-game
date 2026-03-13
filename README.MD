\# Real-Time Secure Multiplayer Game using UDP Socket Programming



\## Project Overview



This project implements a \*\*real-time multiplayer game networking system\*\* using \*\*UDP socket programming\*\* in Python.

The system follows a \*\*client-server architecture\*\* where multiple clients connect to a central server and exchange game state information in real time.



The project demonstrates key \*\*Computer Networks concepts\*\* such as:



\* Socket programming

\* Client-server communication

\* Secure communication using encryption

\* Real-time data transmission

\* Multi-client support

\* Performance evaluation



---



\# Architecture



The system follows a \*\*client-server model\*\*.



```

&nbsp;       +-------------+

&nbsp;       |   Client 1  |

&nbsp;       +-------------+

&nbsp;              |

&nbsp;              |

&nbsp;              v

&nbsp;       +-------------+

&nbsp;       |   Server    |

&nbsp;       | Game Engine |

&nbsp;       +-------------+

&nbsp;          /       \\

&nbsp;         /         \\

&nbsp;+-------------+  +-------------+

&nbsp;|   Client 2  |  |   Client 3  |

&nbsp;+-------------+  +-------------+

```



\### Components



\*\*Server\*\*



\* Handles all client connections

\* Maintains global game state

\* Broadcasts updates to all clients



\*\*Client\*\*



\* Sends player movement

\* Receives game state updates

\* Displays updated positions



\*\*Security Module\*\*



\* Encrypts all messages between client and server



---



\# Technologies Used



\* Python 3

\* UDP Socket Programming

\* JSON Data Exchange

\* Symmetric Encryption



---



\# Project Structure



```

udp-multiplayer-game-cn-project

│

├── client

│   └── client.py

│

├── server

│   └── server.py

│

├── security

│   └── encryption.py

│

├── protocol

│   └── message\_format.md

│

├── tests

│   └── latency\_test.py

│

├── docs

│   ├── project\_report.pdf

│   └── demo\_steps.md

│

├── README.md

├── requirements.txt

└── performance\_results.md

```



---



\# Communication Protocol



\### Join Message



```

{

"type": "join",

"player": "p1"

}

```



\### Move Message



```

{

"type": "move",

"player": "p1",

"x": 10,

"y": 20

}

```



\### Game State Broadcast



```

{

"p1": {"x":10,"y":20},

"p2": {"x":5,"y":8}

}

```



---



\# Installation



\### Step 1 – Clone Repository



```

git clone https://github.com/yourusername/udp-multiplayer-game-cn-project.git

```



\### Step 2 – Navigate to Project



```

cd udp-multiplayer-game-cn-project

```



\### Step 3 – Install Dependencies



```

pip install -r requirements.txt

```



---



\# Running the Project



\### Start Server



```

python server/server.py

```



Output:



```

Server started...

```



\### Start Client



Open another terminal:



```

python client/client.py

```



Example:



```

Enter player id: p1

Move X: 10

Move Y: 20

Game state: {'p1': {'x':10,'y':20}}

```



You can run \*\*multiple clients simultaneously\*\*.



---



\# Performance Evaluation



Testing was conducted with multiple clients connected simultaneously.



| Metric          | Result           |

| --------------- | ---------------- |

| Average Latency | ~30 ms           |

| Throughput      | ~150 packets/sec |

| Packet Loss     | <1%              |



The system maintained stable communication with multiple clients.



---



\# Features



\* Real-time multiplayer synchronization

\* UDP-based communication

\* Multi-client support

\* Encrypted message exchange

\* Game state broadcasting

\* Performance evaluation



---



\# Future Improvements



\* Graphical game interface

\* WASD keyboard controls

\* Packet loss handling

\* Advanced latency optimization

\* TLS secure communication



---



\# Author



Muruli

B.Tech Computer Science Engineering

Computer Networks Mini Project



