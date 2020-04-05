FROM ubuntu:18.04

RUN apt-get update && apt-get upgrade -y && apt-get install --no-install-recommends -y rsync ca-certificates libjansson4 libpng16-16 libzip4 libcurl4 libfreetype6 libfontconfig1 libicu60 wget libzip-dev
RUN wget https://github.com/OpenRCT2/OpenRCT2/releases/download/v0.2.5/OpenRCT2-0.2.5-linux-x86_64.tar.gz
RUN tar xfzv OpenRCT2-0.2.5-linux-x86_64.tar.gz
WORKDIR OpenRCT2
RUN chmod +x openrct2-cli
ENTRYPOINT [ "./openrct2-cli" ]



