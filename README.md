# 🧱 Simple Python Blockchain with Flask

This is a basic implementation of a blockchain using Python and Flask. It allows users to mine blocks and retrieve the full blockchain via a simple REST API.

---

## 🚀 Features

* Mine a block with Proof of Work (PoW)
* Retrieve the entire blockchain
* Hash blocks and validate the chain
* Flask-powered REST API

---

## 🛠️ Technologies Used

| Purpose       | Technology        |
| ------------- | ----------------- |
| Programming   | Python 3          |
| Web Framework | Flask             |
| Cryptography  | hashlib (SHA-256) |
| Data Format   | JSON              |
| Time Handling | datetime module   |

---

## 🧰 Tools Used

* Visual Studio Code 
* Postman 
* Git + GitHub (for version control)
* Python 3.x 

---

## 📦 API Endpoints

### `GET /mine_block`

Mines a new block and adds it to the chain.

**Response:**

```json
{
  "message": "Congratulations ! , You just mined a block.",
  "index": 2,
  "timestamp": "2025-07-21 10:34:56.789012",
  "proof": 5341,
  "previous_hash": "00ab12..."
}
```

---

### `GET /get_chain`

Returns the entire blockchain.

**Response:**

```json
{
  "chain": [...],
  "length": 2
}
```

---

## ✅ How to Run

1. **Clone the repository:**

2. **Install Flask:**

```bash
pip install flask
```

3. **Run the app:**

```bash
python filename.py
```

4. **Test with Postman:**

* [http://localhost:5000/mine\_block](http://localhost:5000/mine_block)
* [http://localhost:5000/get\_chain](http://localhost:5000/get_chain)

---

## 📊 Sample Proof of Work Algorithm

```python
def proof_of_work(previous_proof):
    new_proof = 1
    while True:
        hash_operation = hashlib.sha256(str(new_proof**2 - previous_proof**2).encode()).hexdigest()
        if hash_operation[:4] == '0000':
            return new_proof
        new_proof += 1
```

---

## 📚 License

This project is open-source and free to use for educational purposes.

---

## 🙌 Acknowledgments

* [Python.org](https://python.org)
* [Flask](https://flask.palletsprojects.com/)
* Blockchain concept inspired by educational tutorials
