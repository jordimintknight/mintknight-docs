





{% tabs %}
{% tab title="Node" %}
```javascript
  // 2. Mint 50 tokens to wallet 1.
  task = await mintknight.mintToken(
    project.contractId,
    minter.walletId,
    minter.skey,
	wallet1.walletId,
	'50',
  );
  task = await mintknight.waitTask(task.taskId);
```
{% endtab %}

{% tab title="Python" %}
```
# Install via pip
pip install --upgrade myapi
```
{% endtab %}
{% endtabs %}