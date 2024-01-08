FROM osimis/orthanc:24.1.0-full

# COPY orthanc.json /etc/orthanc/

COPY meddream.py /scripts/meddream.py

ENV ORTHANC__PYTHON_SCRIPT "/scripts/meddream.py"