FROM golang:1.8.1
RUN apt-get update && \
	apt-get install -y python-requests time file sudo && \
	rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN go get \
		github.com/fzipp/gocyclo \
		github.com/golang/lint/golint \
		github.com/kisielk/errcheck \
		github.com/client9/misspell/cmd/misspell && \
	rm -rf /go/pkg/ /go/src/
COPY build.sh /
ENTRYPOINT ["/build.sh"]
