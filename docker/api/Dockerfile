FROM python:3.10-slim
WORKDIR /home
COPY ./requirements_be.txt ./
COPY ./src ./src/
COPY ./models ./models/
COPY ./config ./config/
RUN \
apt update && \
apt upgrade -y && \
apt autoremove -y && \
apt clean -y && \
pip install --upgrade pip && \
pip install wheel && \
pip install -r requirements_be.txt
EXPOSE 8080
CMD ["python", "src/api.py"]