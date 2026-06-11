# devops
from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
    return """
    <h1> DevOps Demo Application</h1>
    <p>Hello! This is my first Dockerized Python Flask app.</p>
    <p>Created by: sandeep</p>
    """

@app.route("/health")
def health():
    return {"status": "UP"}

if __name__ == "__main__":
    app.run(host="0.0.0.0", port=5000)
