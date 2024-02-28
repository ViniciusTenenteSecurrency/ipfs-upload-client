`ipfs-upload-client` is a minimal CLI tool to upload files or directories to Infura's IPFS or another API endpoint.

## Setup

1. Create .env file with the correct URL of the IPFS you want to use:

```
API=http://localhost:5002
```

2. Set the env vars:

```
set -a && source .env && set +a
```

3. Compile and generate exe file:

```
go build
```

## How to run

1. Get the build.zip file and paste it on the root then run:

```
ipfs-upload-client ./build.zip
```

## Check if it was successful uploaded

1. Run the following command replacing the CID on the arg= :

```
curl "http://poc-subgraph.regtoken.io:5002/api/v0/cat?arg=QmTnTHWqRp78Vcxn5fVwEUM3CNtxnyaWxAfYV3UySRcCTr" \
    -X POST \
    --output download.zip
```

2. Unzip download.zip and check the addresses matches