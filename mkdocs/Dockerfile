FROM python
MAINTAINER Dario C <70281924+dario-j-c@users.noreply.github.com>

# Set build directory
WORKDIR /app

# Install dependencies
RUN \
  python -m pip install --upgrade pip && \
  python -m pip install mkdocs-material && \
  pip install mkdocs-glightbox

# Copy files necessary for build
COPY docs docs
COPY includes includes
COPY mkdocs.yml mkdocs.yml

# Set working directory
WORKDIR /app

# Expose MkDocs development server port
EXPOSE 8000

# Start development server by default
ENTRYPOINT ["mkdocs"]
CMD ["serve", "--dev-addr=0.0.0.0:8000"]