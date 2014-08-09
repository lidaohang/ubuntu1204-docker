# 1. Create the user `app`
# 2. Install ruby 2.1.2

FROM jimmychu0807/ubuntu1204:v1
MAINTAINER Jimmy Chu <jimmychu@hkwtf.com>

# Create and switch to user 'app', and switch the corresponding $HOME and $USER
RUN adduser --disabled-password --home /home/app --gecos "" app && \
    su app
USER app
ENV USER app
ENV HOME /home/app

# Install rbenv, ruby 2.1.2. Using rbenv because I am tired of rvm
WORKDIR /home/app
RUN git clone https://github.com/sstephenson/rbenv.git ~/.rbenv && \
    git clone https://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build

RUN echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.profile && \
    echo 'eval "$(rbenv init -)"' >> ~/.profile && \
    echo 'source ~/.profile' >> ~/.bashrc

RUN bash -c -l 'rbenv install 2.1.2'
RUN bash -c -l 'rbenv global 2.1.2' && \
    bash -c -l 'gem install bundler --no-ri --no-rdoc' && \
    bash -c -l 'gem install foreman --no-ri --no-rdoc'
RUN bash -c -l 'rbenv rehash'
ENV RBENV_ROOT /home/app/.rbenv
