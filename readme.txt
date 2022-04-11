Document for using Docker and FastAPI

0. Install Docker
C:\Users\Phulikely>docker -v
Docker version 20.10.14, build a224086


1. Create env
>python -m venv venv
>venv\Scripts\activate.bat


2. Install packages
(venv)>pip install fastapi #framework
(venv)>pip install uvicorn #ASGI server(Asynchronous Server Gateway Interface: Giao diện cổng vào máy chủ không đồng bộ)


3. Create 'main.py' inner of folder 'app'
Copy&paste a simple API from FastAPI website(https://fastapi.tiangolo.com/)


4. Run uvicorn
In a normal way: $ uvicorn main:app --reload
but we can import uvicorn into main.py


5. Create requirements
(venv)>pip freeze > requirements.txt


6. Create Dockerfile
Create 'Dockerfile' (not dockerfile)


7. Fill into Dockerfile


8. Add port and host into main.py
if __name__ == '__main__':
    uvicorn.run(app, port=8000, host='0.0.0.0')


9. Build
(venv)>docker build -t python-fastapi (python-fastapi is just a name)
(venv)>docker build -t python-fastapi .


10. Run
(venv)>docker run -p 8000:8000 python-fastapi


11. Check
http://127.0.0.1:8000/
(or using Docker Desktop)
