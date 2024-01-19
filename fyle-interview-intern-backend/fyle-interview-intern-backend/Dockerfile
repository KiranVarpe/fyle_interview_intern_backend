from python:3.8
workdir .
copy . .
run pip install virtualenv 
run pip install flask
run pip install -r requirements.txt
ENV FLASK_APP="core/server.py"
run rm core/store.sqlite3
expose 7755
run flask db upgrade -d core/migrations/
cmd ["pytest","--cov"]


