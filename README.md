from flask import Flask
from threading import Thread


app=Flask(_name_)

@app.route('/')
def hello():
    return 'Hello, World! '


def run_app():
    app.run(debug=true, use_reloader=False, host='0.0.0.0', port=5000)
    
thread = Thread(target=run_app)
thread.start()
