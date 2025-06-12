FROM python:3.14

RUN useradd -m -s /bin/bash codespace
RUN usermod -aG sudo codespace && \
    echo "codespace ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers
USER codespace

RUN curl -LsSf https://astral.sh/uv/install.sh | sh
ENV PATH="/home/codespace/.local/bin:$PATH"

WORKDIR /workspaces/time-mcp-server-codespaces

EXPOSE 3000 5000 8000

CMD ["bash"]