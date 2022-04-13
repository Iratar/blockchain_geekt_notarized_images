HOW to start new project with TRUFFLE

1. npm i -g truffle
2. mkdir Geekt
3. cd Geekt
4. truffle init         (it will create all folders and add '1_initial_migration.js' file to Migrations folder)
5. add new file with your smart contract 'Geekt.sol'


HOW to deploy

1. install GANACHE
2. run Ganache in your OS 
3. create file '2_deploy_contracts.js'
4. copy content from '1_initial_migration.js' into '2_deploy_contracts.js'.
5. in the file '2_deploy_contracts.js' replace 'Migrations' by you contact name
6. truffle migrate


HOW to test your smart contract from console

1. truffle console
2. Geekt = Geekt.deployed()
3. Geekt.then(function(instance){return JSON.stringify(instance.abi);})
4. Geekt.then(function(instance){return instance.registerNewUser("Tectract","Denver","CO","USA");})
5. Geekt.then(function(instance){return instance.addImageToUser('www.myimageURL.com','0x6c3e007e281f6948b37c511a11e43c8026d2a16a8a45fed4e83379b66b0ab927');})
6. Geekt.then(function(instance){return instance.getUser('0x0ac21f1a6fe22241ccd3af85477e5358ac5847c2');}) 
7. Geekt.then(function(instance){return instance.getUsers();})
8. Geekt.then(function(instance){return instance.getImages();})
9. Geekt.then(function(instance){return instance.getImage('0x6c3e007e281f6948b37c511a11e43c8026d2a16a8a45fed4e83379b66b0ab927');})