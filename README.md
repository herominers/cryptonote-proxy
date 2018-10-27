# HeroMiners Proxy Mining Control https://herominers.com
cryptonote-proxy

![switch](https://images2.imgbox.com/07/ce/H4UckRqP_o.png)

Support: https://discord.gg/gvWSs84


# Windows Installation Guide


cryptonote-proxy is a node.js program written by Seb Green that acts as a link between cryptonight mining software and the pool. Typically it is used by most users to quickly change pools without needing to restart their mining software. It can be used for any pool requiring the cryptonight algorithm (most cryptonote coins use this algorithm).
		
A stratum-capable cryptonight mining software (eg. xmrstak, xmrig, cast-xmr etc.) is required to make use of cryptonote-proxy. When in doubt, any third-party mining software (i.e. not the one that came with your coin's daemon or wallet), is a stratum-capable miner.
		
This guide is written with Debian/Ubuntu Linux in mind. However, it can be used for any Linux distro, by substituting the package manager-specific commands with the ones used by your distro.

<h2>1. Download and install the latest nodejs version from <a target="_blank" href="https://nodejs.org/en/" title="NodeJs" alt="NodeJs" rel="nofollow">https://nodejs.org/en/</a></h2>
		
  ![switch](https://images2.imgbox.com/70/56/iJhxsSJc_o.png)
		
		
<h2>2. Download and install Git for Windows - <a target="_blank" title="git-scm" alt="git-scm" rel="nofollow" href="https://git-scm.com/download/win">https://git-scm.com/download/win</a></h2>

During package installation, deselect the both options as shown (we don’t need that)
		
![switch](https://images2.imgbox.com/4b/a5/hlbS8B18_o.png)
		
		
Use Git from Windows Command Prompt
	
![switch](https://images2.imgbox.com/e8/9c/CgbXQPCf_o.png)

Then everything else, is just next, next, next and install.
		
		
Now open command prompt by going Search, type cmd, enter
	
		
<blockquote>
<b>
git clone https://github.com/herominers/cryptonote-proxy.git
</b>
</blockquote>
	
	
![switch](https://images2.imgbox.com/e0/3a/N43SNE0R_o.png)
	
	
<blockquote>
<b>
cd cryptonote-proxy
</b>
</blockquote>
	
	
![switch](https://images2.imgbox.com/af/81/RMi55BXd_o.png)
	
	
Cd to the cryptonote-proxy source directory and run npm update
	
	
<blockquote>
<b>
npm update
</b>
</blockquote>
	
	
![switch](https://images2.imgbox.com/2b/b9/C2zoH5cQ_o.png)
	
	
Go to directory of cryptonote-proxy, open config.json and edit the pool settings.
	
	
![switch](https://images2.imgbox.com/3d/a4/7RDKvKFp_o.png)


Save the <b>config.json</b>
	
	
To run the proxy, double click <b>run.sh</b>


![switch](https://images2.imgbox.com/d3/f8/3s3I7eCs_o.png)


At this point of time, you can open the browser and the address would be <a target="_blank" href="http://localhost:2350" title="windows" alt="windows">http://localhost:2350</a>
	
If you are opening from another computer within the local network (eg. 192.168.1.x network),
		
Use <a target="_blank" href="http://192.168.1.77:2350" title="windows" alt="windows">http://192.168.1.77:2350</a> (If your proxy server IP is 192.168.1.77) If you can see this page, congratulations!


		
![switch](https://images2.imgbox.com/5d/89/fM0gNgd4_o.png)
		
		
		
		
![switch](https://images2.imgbox.com/db/4d/m8iMXVAI_o.png)
		
		
Now we have to configure miner config to use proxy server. For example i’m using XMRIG in this case.


Now run the miner.


![switch](https://images2.imgbox.com/da/44/F2xfO7fD_o.png)
		

One of the pool should be selected by default. Click on whichever pool you want to mine on and start the your miner.

Until you close cryptonote-proxy, you can switch between pools without shutting down your miner or even add new pools to config.json.

Now you are able to enjoy the switching from coin to coin with just <b>1 single mouse click.</b> 

That’s it!

  
  
  
  
# Linux Installation Guide: https://graft.herominers.com/#linux



<h2>1. Installation of the required software.</h2>


If you haven't updated your linux install in a long time (or are running into errors in the next few steps), it is a good idea to update/upgrade your system:
		
<blockquote>
<b>
$ sudo apt-get update
<br/>
$ sudo apt-get upgrade
</b>
</blockquote>
		
	
Next we need to install git, node.js, and nano.


<blockquote>
<b>
$ sudo apt-get install git nodejs nano
</b>
</blockquote>


<b>Node.js</b> is required for cryptonote-proxy to work. 


<b>Git</b> is a convenience, and will make this guide a lot easier to follow. 


If you do not wish to install git, you'll have to download and extract the cryptonote-proxy manually from <a target="_blank" title="Cryptonote Proxy" alt="Cryptonote Proxy" rel="nofollow" href="https://github.com/herominers/cryptonote-proxy">https://github.com/herominers/cryptonote-proxy</a> 


<b>Nano</b> is simply an easy-to-use console-base text editor. If you are running a desktop version of Linux or have a Bash on Windows installation of Linux, you can skip installing this.

		
We can now clone the latest version of cryptonote-proxy from github and install its dependencies using the node.js package manager (npm):


<blockquote>
<b>
$ cd ~

$ git clone https://github.com/herominers/cryptonote-proxy.git


$ cd cryptonote-proxy


$ npm i

</b>
</blockquote>
		
		
Replace <b>"cd ~"</b> with your preferred install directory. 


Git will create a sub-directory under this directory. If there are no errors so far, then you have successfully installed cryptonote-proxy.


![switch](https://images2.imgbox.com/1c/03/Tvn1gVkI_o.png)	
		

<h2>2. Configuring your 'cryptonote-proxy'</h2>

Copy the example config file, and open it up in nano (or your favorite text editor):

		
<blockquote>
<b>
$ nano config.json
</b>
</blockquote>
		


![switch](https://images2.imgbox.com/b4/53/8VZra3aE_o.png)
		

<blockquote>
<b>
For Bash on Windows Users: you can find your linux rootfs at: C:\Users\USERNAME\AppData\Local\Packages\CanonicalGroupLimited.UbuntuonWindows_11erwerewfef\LocalState\rootfs
</b>
</blockquote>
		
<blockquote>
<b>
However, it is not recommended that you edit files in your Linux rootfs directly from Windows. 

This is due Windows programs not handling the extra permission features used by Linux correctly (Editing Window’s file from within Linux is fine). 

To use Window-based text editing software, it is better to copy config.json to your desktop, edit it.

Then copy it back over to your linux rootfs (e.g. “$ cp /mnt/c/USERNAME/Desktop/config.json .”). If you do edit the file directly from Windows, you’ll need to run “$ chmod +rw config.json” to reset the file permission correctly – don’t turn this into a habit or it’ll get messy quick!
</b>
</blockquote>
				
		
Inside your config.json, you'll see a couple of options and a list of sample pools, which you'll have to replace with your own. Leave the option for <b>"workerport"</b> and <b>"httpport"</b> alone for now.

Under the "pools" option tree you'll see <b>"userA"</b> and <b>"userB"</b>. You can change <b>"userA"</b> and <b>"UserB"</b> to whatever you want.

If you do not have a multi-rig setup or not planning on connecting to two different pool at the same time, you can delete the entire tree under <b>"userB"</b>.

Each pool has an entry that looks like this:


<blockquote>
<b>
{
"symbol":"Graft",

"name":"GAhmkFwdUqLW6cKUwjH44scujPpb2kS4yWSrLhSYAj1zdLXkvsnUmrFTSFJ45sAi1AY1eN1rs4N6QQbGxxcAGjndMyrUMi4",

"host":"graft.herominers.com",

"port":"10100",

"url":"https://graft.herominers.com",

"api":"https://graft.herominers.com/api"
},
</b>
</blockquote>

		
Configuring this is fairly straightforward if you have used mining software before.

"symbol" is the name of your coin. You can use ticker symbol, full name, pool name, or whatever you like. 

One of these can be set to the "default" option above, which will auto-select that pool when you start cryptonote-proxy.

"url" is the url of the pool (for example: https://graft.herominers.com). If the pool supports it, this will also autofill your wallet info in its stat tracker.

"api" is the pool api where your proxy pull to display additional stats (for example: https://graft.herominers.com/api)

Save the file once done (Press <b>Ctrl-X</b> in nano to exit and save).



<h3>3. Configuring your mining software.</h3>

If the proxy is being run on the same machine as the miner: Point your pool address to <b>"localhost:2349"</b> set <b>"UserA"</b> (or whatever username you defined in the proxy) as your user/wallet address Password is used to identify your worker in cryptonote-proxy.


In xmr-stak, your config.txt should have something like the following entry under "pool_list":

		
<blockquote>
<b>
{
"pool_address" : "localhost:2349", "wallet_address" : <font class="colorred">"userA"</font>, "pool_password" : "myRig1", "use_nicehash" : false, "use_tls" : false, "tls_fingerprint" : "", "pool_weight" : 1 
},
</b>
</blockquote>
		
		
Any number of mining instances can be pointed to cryptonote-proxy.

If you're connecting your miner from a different machine, replace "localhost" with the ip of the machine running cryptonote-proxy.
	
		
<h3>4. Running/Using</h3>

start cryptonote-proxy:

<blockquote>
<b>
$ node proxy.js
</b>
</blockquote>
		

Open up your browser to <b>"localhost:2350"</b> if cryptonote-proxy is located on the same machine, otherwise, replace localhost with the ip of the machine cryptonote-proxy is being run on. 

Enter <b>“UserA”</b> (or whatever you set it to) and hit load and you should see something similar to the screen below:

<a target="_blank" href="http://localhost:2350"><b>http://localhost:2350</b></a>



![switch](https://images2.imgbox.com/5d/89/fM0gNgd4_o.png)



![switch](https://images2.imgbox.com/db/4d/m8iMXVAI_o.png)



Now we have to configure miner config to use proxy server. For example i’m using XMRIG in this case.

Now run the <b>miner.</b>


![switch](https://images2.imgbox.com/da/44/F2xfO7fD_o.png)



One of the pool should be selected by default. Click on whichever pool you want to mine on and start the your miner.

Until you close cryptonote-proxy, you can switch between pools without shutting down your miner or even add new pools to config.json.

Now you are able to enjoy the switching from coin to coin with just <b>1 single mouse click.</b> 

That’s it!



