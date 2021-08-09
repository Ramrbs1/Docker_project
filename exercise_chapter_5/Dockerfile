FROM python:3.7.3-stretch

## Complete Step 1:
WORKDIR /app

## Complete Step 2:
# Copy source code to working directory
COPY flask_app/web.py /app/
COPY requirements.txt /app/
COPY  nlib /app/nlib
## Complete Step 3:
# Install packages from requirements.txt
# hadolint ignore=DL3013
RUN pip install --upgrade pip &&\
    pip install --trusted-host pypi.python.org  -r requirements.txt
    

EXPOSE 80

## Complete Step 5:
# Run app.py at container launch
CMD ["python", "web.py"]
