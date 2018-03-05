# bitcore-serviceskeleton
The skeleton of bitcore service

In order to write service with bitcore, you just need to fork this repo, then add your code.

## Usage
[Follow this guide](https://bitcore.io/guides/full-node/) to install and run a full Bitcore node.

Assuming the created Bitcore node is called ___mynode___ and resides in your home directory

```bash
cd ~/mynode/node_modules
git clone https://github.com/qinfengling/bitcore-serviceskeleton.git sampleservice
cd sampleservice
npm install
```

Add ___sampleservice___ as a dependency in ~/mynode/bitcore-node.json

```javascript
{
  "datadir": "./data",
  "network": "testnet",
  "port": 3001,
  "services": [
    "db",
    "address",
    "sampleservice"
  ]
}
```

Start bitcore-node, then you can access the service with `http://localhost:3001/sampleservice`
