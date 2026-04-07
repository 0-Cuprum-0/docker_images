FROM python:3.11-slim
WORKDIR /token
RUN pip install uv
RUN uv venv
RUN apt-get update && apt-get install -y git
RUN git clone https://codeberg.org/argrento/huami-token.git
WORKDIR huami-token
RUN uv pip install --system -e ".[dev]"
CMD ["bash"]
