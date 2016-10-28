FROM ruby:2.3.1
MAINTAINER Joe-noh

RUN \
  cd /tmp && \
  wget http://nodejs.org/dist/latest-v6.x.tar.gz && \
  tar xvzf latest-v6.x.tar.gz && \
  rm -f latest-v6.x.tar.gz && \
  cd node-v* && \
  ./configure && \
  CXX="g++ -Wno-unused-local-typedefs" make && \
  CXX="g++ -Wno-unused-local-typedefs" make install && \
  cd /tmp && \
  rm -rf /tmp/latest-* && \
  npm install -g npm && \
  echo -e '\n# Node.js\nexport PATH="node_modules/.bin:$PATH"' >> /root/.bashrc

RUN npm install -g bower grunt-cli
