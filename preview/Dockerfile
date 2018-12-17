FROM alpine:edge

# http://bugs.python.org/issue19846
# > At the moment, setting "LANG=C" on a Linux system *fundamentally breaks Python 3*, and that's not OK.
ENV LANG C.UTF-8

ENV WEASYPRINT_VERSION=44

RUN apk add --no-cache gcc musl-dev jpeg-dev zlib-dev libffi-dev cairo-dev pango-dev gdk-pixbuf python3-dev fontconfig ttf-opensans ca-certificates

RUN pip3 install weasyprint==$WEASYPRINT_VERSION

CMD [ "weasyprint", "--version" ]
