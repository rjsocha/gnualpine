# syntax=docker/dockerfile:1.6
FROM alpine:3 AS mold
RUN apk --no-cache -U upgrade && \
    apk --no-cache -U add bash coreutils findutils tar wget curl sed gawk diffutils grep

FROM scratch
COPY --from=mold / /
CMD ["/bin/bash" ]
