ARG JITSI_REPO=rvolosatovs
ARG BASE_TAG=latest
FROM ${JITSI_REPO}/jitsi-base-java:${BASE_TAG}

ENV GOOGLE_APPLICATION_CREDENTIALS /config/key.json

RUN \
	apt-dpkg-wrap apt-get update && \
	apt-dpkg-wrap apt-get install -y jigasi jq && \
	apt-cleanup

COPY rootfs/ /

VOLUME ["/config", "/tmp/transcripts"]
