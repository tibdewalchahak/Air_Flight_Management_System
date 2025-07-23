# ✈️ Air Flight Management System (Using two different Data Structures)

This project demonstrates a **Air Flight Management System** implemented using **two different data structures**:  
- **Linked List Bucketing**
- **AVL Tree (Self-Balancing BST)**

The goal is to compare how different data structures affect the organization, insertion, and retrieval of flight data — helping you better understand their practical applications in real-world scenarios. It was developed as part of the Data Structures and Program Design II course to strengthen the understanding of core DSA concepts like Linked List, Trees, Algorithms and file handling through a real-world use case.

---

## 📂 Project Structure
  Air_Flight_Management_Linked_List_S24.c - Using Linked List
  
  Air_Flight_Management_Trees_S24.c - Using AVL Trees
  
## 🚀 Functionality
Both versions:
- Read flight records from a CSV file
- Store flights based on departure time
- Group flights into time intervals (e.g. buckets of 1 hour each)
- Sort and display flights within each bucket

---

## 🧠 Data Structures Used

### 1. ✅ **Linked List Bucketing**
- **Data Structure**: Custom buckets linked via `bucketNode`, each containing a `flightNode` list.
- **Purpose**: Group flights into specific time intervals and maintain sorted order.
- **Pros**:
  - Simple to implement
  - Good for sequential insertion and time-slot grouping

### 2. 🌲 **AVL Tree**
- **Data Structure**: Self-balancing Binary Search Tree (AVL) where each node stores a flight record.
- **Purpose**: Maintain sorted order while ensuring balanced height for faster operations.
- **Pros**:
  - Guaranteed O(log n) insertion, deletion, and search
  - Auto-balancing improves performance over plain BST
---

## 🧪 Input Format

A sample `input.csv` file is required in each version. Format:

```csv
FlightNumber, DepartureTime, ArrivalTime
AI101, 01:45, 04:30
AI102, 07:15, 09:45
...
```
Time should be in 24-hour HH:MM format.

## 🛠️ How to Run
## 🔗 Linked List Version
```bash
gcc Air_Flight_Management_Linked_List_S24.c -o flight
./flight input.csv
```
## 🌳 Tree Version
```bash
gcc Air_Flight_Management_Trees_S24.c -o flight
./flight input.csv
```

## 📊 Comparison Insights

| Feature             | Linked List Bucketing              | AVL Tree (Self-Balancing BST)       |
|---------------------|-------------------------------------|--------------------------------------|
| Insertion Time      | O(n) (due to sorting in bucket)     | O(log n) (guaranteed)                |
| Search Efficiency   | O(n)                                | O(log n)                             |
| Ordered Traversal   | Requires explicit sorting           | In-order traversal (auto sorted)     |
| Balancing Needed    | Not applicable                      | Automatic after every insertion      |
| Memory Overhead     | Higher (extra bucket structs)       | Efficient (balanced tree nodes)      |
| Code Complexity     | Moderate                            | Higher (due to rotations)            |


## 📚 Learning Outcome
This project helps solidify understanding of:
- How different data structures impact performance
- Trade-offs between simplicity and scalability
- Real-world structuring of data (like scheduling systems)

## 📚 Academic Context
This project was completed as part of the "Data Structures and Program Design II" course in the 2nd year of B.Tech in Computer Science and Engineering.
