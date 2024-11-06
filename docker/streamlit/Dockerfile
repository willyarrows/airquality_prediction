FROM python:3.10-slim
WORKDIR /home
COPY ./requirements_fe.txt ./
COPY ./src ./src/
COPY ./assets ./assets/
RUN \
apt update && \
apt upgrade -y && \
apt autoremove -y && \
apt clean -y && \
pip install --upgrade pip && \
pip install wheel && \
pip install -r requirements_fe.txt
EXPOSE 8501
CMD ["streamlit", "run", "src/streamlit.py"]