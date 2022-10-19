FROM ubuntu:20.04

RUN apt update && apt upgrade -y && apt install curl -y
RUN touch install.sh && chmod +x install.sh && curl -o install.sh -sSfL https://release.solana.com/v1.14.3/install
RUN sh -c ./install.sh 
ENV PATH="/root/.local/share/solana/install/active_release/bin:${PATH}"
CMD [ "solana-test-validator" ]