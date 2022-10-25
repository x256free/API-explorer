<h1 class="code-line" data-line-start=0 data-line-end=1 ><a id="APIexplorer_0"></a>API-explorer</h1>
<p class="has-line-data" data-line-start="1" data-line-end="2">FastyChain api explorer</p>
<h1 class="code-line" data-line-start=3 data-line-end=4 ><a id="EXAMPLE_3"></a>EXAMPLE</h1>
<p class="has-line-data" data-line-start="4" data-line-end="17"><strong>REQUEST</strong><br>
/address/{address} (<a href="https://fastychain.com/api/address/0x0000000000000000000000000000000000000000">https://fastychain.com/api/address/0x0000000000000000000000000000000000000000</a>)<br>
<strong>RESPONSE</strong><br>
address<br>
balance <em>(ETHER format)</em><br>
balance_wei <em>(WEI format)</em><br>
updated_at <em>(YYYY-MM-GG T HOUR:MIN:SECONDS)</em><br>
total_supply <em>(for smart contracts)</em><br>
contract <em>(Is a contract?)</em><br>
erc_types <em>(for smart contracts)</em><br>
interfaces <em>(for smart contracts)</em><br>
number_of transactions<br>
attached_contract <em>(details about compile/verify of the contract, if “valid”: false, smart contract not verified.)</em></p>
<h1 class="code-line" data-line-start=18 data-line-end=19 ><a id="LIST_18"></a>LIST</h1>
<p class="has-line-data" data-line-start="19" data-line-end="20"><strong>GET REQUESTS</strong></p>
<p class="has-line-data" data-line-start="21" data-line-end="30"><strong>ADDRESS</strong><br>
/address/{address}/transactions<br>
/address/{address}/owned_tokens<br>
/address/{address}/holders<br>
/address/{address}<br>
/address/{address}/internal_transactions<br>
/address/{address}/contract<br>
/address/{address}/tx/{nonce}<br>
/address/{address}/tx/{nonce}/hash</p>
<p class="has-line-data" data-line-start="31" data-line-end="36"><strong>BLOCKS</strong><br>
/blocks/{num}/transactions<br>
/blocks/{hash}<br>
/blocks/{num}<br>
/blocks</p>
<p class="has-line-data" data-line-start="37" data-line-end="44"><strong>GENERAL</strong><br>
/stats<br>
/richlist<br>
/signersStats<br>
/transaction/{hash}<br>
/signersList<br>
/supply</p>
<p class="has-line-data" data-line-start="45" data-line-end="47"><strong>POST REQUEST</strong><br>
/verify</p>
<pre><code class="has-line-data" data-line-start="48" data-line-end="57">{
    &quot;address&quot;: &quot;&quot;, //contract address
    &quot;contract_name&quot;: &quot;&quot;, 
    &quot;compiler_version&quot;: &quot;0.5.16&quot;, //solidity version
    &quot;evm_version&quot;: &quot;byzantium&quot;,
    &quot;optimization&quot;: true, //(bool)
    &quot;source_code&quot;: &quot;&quot; //source code, replace enter with \n and &quot; with \&quot;
}
</code></pre>
