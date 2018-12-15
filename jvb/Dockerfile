ARG JITSI_REPO=rvolosatovs
ARG BASE_TAG=latest
FROM ${JITSI_REPO}/jitsi-base-java:${BASE_TAG}

RUN \
	apt-dpkg-wrap apt-get update && \
	apt-dpkg-wrap apt-get install -y jitsi-videobridge2 jq curl iproute2 && \
	apt-cleanup

COPY rootfs/ /

VOLUME /config
