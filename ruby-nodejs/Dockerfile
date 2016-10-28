FROM ruby:2.3.1
MAINTAINER Joe-noh

RUN \
  cd /tmp && \
  wget http://nodejs.org/dist/latest-v6.x/node-v6.9.1.tar.gz && \
  tar xvzf node-v6.9.1.tar.gz && \
  rm -f node-v6.9.1.tar.gz && \
  cd node-v* && \
  ./configure && \
  CXX="g++ -Wno-unused-local-typedefs" make && \
  CXX="g++ -Wno-unused-local-typedefs" make install && \
  cd /tmp && \
  rm -rf /tmp/node-v* && \
  npm install -g npm && \
  echo -e '\n# Node.js\nexport PATH="node_modules/.bin:$PATH"' >> /root/.bashrc

RUN npm install -g bower grunt-cli
