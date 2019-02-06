from flask import Flask
from flask import request
from flask import render_template

from led import turnLed

app = Flask(__name__)
 
@app.route("/")
def hello():
	return render_template('web.html')
	return "Hello Our Team!"

@app.route("/led")
def led():
	status = request.args.get('status')
	if status == "on":
		turnLed(True)
	else:
		turnLed(False) 
	return "Satisfied Your Request!!"
 
if __name__ == "__main__":
	app.run(host='localhost', port=8080)
