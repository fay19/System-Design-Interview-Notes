# FaceBook Messenger

## What is Facebook Messenger
A software application which provides text-based instance messaging service to its users.  

## Requirements and Goals of the system
### Functional Requirements
1. support one-on-one conversations between users
2. keep track of online/offline statuses of its users
3. support persistent storage of chat history

### Non-functional Requirements
1. low latency
2. highly consistent - user should see same chat history on all their devices
3. high avaliability is desirable; low avaliability is tolerable in the interest of consistency

### Extented Requirments
1. Group chats
2. Push notifications

## Capacity Estimation and Constraints
- Assume 500 million active daily users
- Each user send 40 messages in average per day
- In total, 20 billion messages per day

### Storage Estimation
- Assume each message is 100 bytes
- Daily increase: 20 billion * 100 bytes => 2TB/day
- Store 5 years: 2TB * 365 days * 5 years => 3.6 PB
- Metadata(userId, timestamp...) is not considered yet
- data compression and replication not considered yet

### Bandwidth Estimation
- 2TB each day, 2TB/86000sec ~= 25MB/s

## High Level Design
![online-chat])(../images/online-chat.jpg)

## Detailed Component Design

### Start with small
- Everything runs on one server
- Functions
  - Receive incoming messages and deliver outgoing messages
  - Store and retrieve messages from the database
  - Keep a record of user online/offline status, and notify all the relevant users about these status changes
  
### Message Handling

