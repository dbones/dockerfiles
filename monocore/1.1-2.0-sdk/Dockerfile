FROM microsoft/aspnetcore-build:1.0-2.0

ENV MONO_VERSION 5.8.0.127

RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF

RUN echo "deb http://download.mono-project.com/repo/debian stable-jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list \
  && apt-get update \
  && apt-get install -y mono-complete \
  && rm -rf /var/lib/apt/lists/* /tmp/*