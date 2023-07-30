FROM rust:latest

WORKDIR /app

RUN apt update -y \
  && apt install -y \
     libwebkit2gtk-4.0-dev \
     build-essential \
     curl \
     wget \
     file \
     libssl-dev \
     libgtk-3-dev \
     libayatana-appindicator3-dev \
     librsvg2-dev \
     fonts-noto-cjk \
     ibus-mozc \
  && curl -fsSL https://deb.nodesource.com/setup_20.x | bash - \
  && apt-get install -y nodejs \
  && npm install -g yarn \
  && cargo install create-tauri-app

# RUN echo 'export GTK_IM_MODULE=ibus' >> ~/.bashrc \
#     echo 'export XMODIFIERS=@im=ibus' >> ~/.bashrc \
#     echo 'export QT_IM_MODULE=ibus' >> ~/.bashrc \
#     echo 'ibus-daemon -drx' >> ~/.bashrc
