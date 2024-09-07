FROM alpine

RUN apk fix && \
    apk --no-cache --update add git git-lfs openssh && \
    git lfs install
ADD .gitconfig /root/.gitconfig


FROM scratch

COPY --from=0 / /
CMD [ "/bin/sh" ]
