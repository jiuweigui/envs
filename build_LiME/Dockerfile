FROM build/arm-eabi-4.6:v1.1

# Move sourcecode to the docker image$
ADD src/* /tmp/src/

# Share out$
VOLUME /tmp/out$

# Set working directory, entrypoint and run make$
WORKDIR /tmp/src/src
ENTRYPOINT ["make"]
