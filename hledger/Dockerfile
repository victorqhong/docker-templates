FROM haskell as builder

COPY hledger-install.sh /usr/local/bin
RUN bash hledger-install.sh

FROM haskell
COPY --from=builder /root/.local/bin/ /usr/local/bin/

CMD ["hledger-web", "--server"]
