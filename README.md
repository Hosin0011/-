# -from flask import Flask, jsonify, request

app = Flask(__name__)

@app.route('/api/square', methods=['POST'])
def square_number():
    data = request.get_json()
    number = data.get('number')
    result = number ** 2
    return jsonify({'result': result})

if __name__ == '__main__':
    app.run()
