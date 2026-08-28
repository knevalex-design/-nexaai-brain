from flask import Flask, jsonify
import random
from datetime import datetime

app = Flask(__name__)

@app.route('/')
def home():
    return jsonify({
        "status": "NexaAI LIVE",
        "owner": "Nevalex",
        "strategy": "Double MACD",
        "message": "Cerveau en ligne"
    })

@app.route('/analyze')
def analyze():
    signal = random.choice(["BUY", "SELL", "WAIT"])
    conf = random.randint(80, 96)
    return jsonify({
        "pair": "XAUUSD",
        "signal": signal,
        "confidence": f"{conf}%",
        "time": str(datetime.now())
    })

if __name__ == '__main__':
    app.run(host='0.0.0.0', port=10000)
