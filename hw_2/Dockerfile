FROM ubuntu:22.04
RUN apt update
RUN cd /
RUN echo Y | apt install python3 pip sqlite3 git systemctl
RUN git clone https://github.com/Garpusha/smart_home.git
RUN pip install -r /smart_home/requirements.txt
RUN python3 /smart_home/manage.py migrate
CMD ["python3", "/smart_home/manage.py", "runserver", "0.0.0.0:8000"]
