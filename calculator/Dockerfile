FROM python:latest
WORKDIR /app
COPY . . 
RUN pip install --upgrade pip
RUN pip install Flask 
RUN pip install -r requirements.txt
EXPOSE 8000
ENV FLASK_APP=app.py    
CMD ["python","app.py"]

