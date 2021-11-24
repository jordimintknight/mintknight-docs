### How to mint a NFT

```javascript

  // Add a new admin user.
  const user = await mintknight.addUser(conf.email, conf.password, conf.phone);

  // Login as admin to knitghnight to get the user API KEY.
  console.log(conf);
  let result = await mintknight.loginUser(conf.email, conf.password);
  conf.token = result.token;

  // Add a new company for that user.
  const company = await mintknight.setCompany(
    process.env.COMPANY_NAME,
    process.env.COMPANY_TAXID,
    process.env.COMPANY_ADDRESS,
    process.env.COMPANY_COUNTRY,
  );
  conf.companyId = company._id;

  // Add a new project.
  const project = await mintknight.addProject(
    process.env.PROJECT_NAME,
    process.env.PROJECT_DESCRIPTION,
    process.env.PROJECT_NETWORK,
  );
  conf.projectId = project._id;

  // Get the API KEY from that project.
  const apiKey = await mintknight.getApiKey(conf.projectId);
  conf.apiKey = apiKey.token;

  
  // Add wallet : minter for the contracts. Th id is internal to your organization.
  let task = await mintknight.addWallet('id_minter');
  const minter = { walletId: task.wallet._id, skey: task.skey1 };
  task = await mintknight.waitTask(task.taskId);
  minter.address = task.addressTo;
  fs.writeFileSync( path.join(__dirname, 'json', 'minter.json'), JSON.stringify(minter), 'utf8')


 // Add the NFT contract to the project.
  let task = await mintknight.deployContract(
    721,
    process.env.NFT_NAME,
    process.env.NFT_SYMBOL,
    process.env.NFT_DESCRIPTION,
    minter.walletId,
  );
  task = await mintknight.waitTask(task.taskId);
  project.nftAaddress = task.addressTo;
  fs.writeFileSync( path.join(__dirname, 'json', 'nft.json'), JSON.stringify(project), 'utf8');

// Upload 1 NFT to wallet 1.
  task = await mintknight.uploadNFT(
    project.nftId,
    'NFT #2',
    'First NFT to be created on Mintknight',
    [{
        trait_type: "XP",
        value: "100"
      }, {
        trait_type: "Color",
        value: "blue"
    }],
    './assets/image.png'
  );
  
  task = await mintknight.waitTask(task.taskId); 


// Mint NFT



```