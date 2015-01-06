FROM platanus/rbenv

MAINTAINER Juan Ignacio Donoso "juan.ignacio@platan.us"

ENV RUBY_ALIAS 2.0.0
ENV RUBY_VERSION 2.0.0-p598

# skip installing gem documentation
RUN echo 'gem: --no-document' >> "$HOME/.gemrc"

# install ruby and set it as global version
RUN rbenv install $RUBY_VERSION && ln -s $RBENV_ROOT/versions/$RUBY_VERSION $RBENV_ROOT/versions/$RUBY_ALIAS
RUN rbenv global $RUBY_ALIAS

# Install bundler
RUN gem install bundler

CMD [ "irb" ]
