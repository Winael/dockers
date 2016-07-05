FROM didrocks/snapcraft:latest
RUN apt update -y && apt update
RUN apt install -y snapd git snapcraft nano bzr
RUN addgroup admin
ENV HOME /home/snapcraft
RUN useradd --create-home --home-dir $HOME --groups admin snapcraft \
         && chown -R snapcraft:snapcraft $HOME
RUN echo 'snapcraft ALL=(ALL) NOPASSWD:ALL' > /etc/sudoers.d/snapcraft
USER snapcraft
WORKDIR $HOME
