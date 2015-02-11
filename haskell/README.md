# Dockerfile - tattsun/haskell
This dockerfile contains latest haskell package based on ubuntu:latest

## Example

```
FROM tattsun/haskell:latest

WORKDIR /root

# install dependencies
ADD ./your-project.cabal /root/your-project.cabal
RUN cabal update && cabal install --only-dependencies

# install
ADD ./ /root
RUN cabal install --force-reinstalls

# execute
CMD ["/root/.cabal/bin/your-project"]

```
