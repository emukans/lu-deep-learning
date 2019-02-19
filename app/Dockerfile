FROM python:3.6

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

COPY requirements.txt /usr/src/app/

RUN pip install --no-cache-dir -r requirements.txt

COPY . /usr/src/app
COPY config/jupyter_notebook_config.py /root/.jupyter/jupyter_notebook_config.py

ENTRYPOINT ["jupyter", "notebook", "--ip=0.0.0.0", "--allow-root"]
