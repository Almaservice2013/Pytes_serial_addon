FROM python:3.9-slim

# Set environment variables
ENV LANG=C.UTF-8
ENV LC_ALL=C.UTF-8

# Install dependencies
RUN pip install --no-cache-dir homeassistant \
    && pip install --no-cache-dir configparser==7.0.0 \
    && pip install --no-cache-dir DateTime==5.5 \
    && pip install --no-cache-dir pytz==2024.1 \
    && pip install --no-cache-dir zope.interface==6.4.post2 \
    && pip install --no-cache-dir setuptools==70.3.0 \
    && pip install --no-cache-dir mysql-connector==2.2.9 \
    && pip install --no-cache-dir paho-mqtt==2.1.0 \
    && pip install --no-cache-dir pipdeptree==2.23.1 \
    && pip install --no-cache-dir packaging==24.1 \
    && pip install --no-cache-dir pip==24.1.2 \
    && pip install --no-cache-dir pyserial==3.5 \
    && pip install --no-cache-dir wheel==0.43.0

# Copy addon files
COPY . /app
WORKDIR /app

# Run the addon
CMD ["python", "pytes_serial.py"]
