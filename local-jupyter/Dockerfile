FROM python:3
ADD jupyter_notebook_config.json /root/.jupyter/
WORKDIR /app
RUN pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir jupyter
RUN apt-get install -y git
RUN git clone https://github.com/PythonistaMX/py261
EXPOSE 8888 8000
CMD ["jupyter", "notebook", "--no-browser", "--ip=0.0.0.0", "--allow-root", "--NotebookApp.allow_password_change=False"]