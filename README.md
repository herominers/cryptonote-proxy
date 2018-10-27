# HeroMiners Proxy Mining Control
cryptonote-proxy


Support: https://discord.gg/gvWSs84

Windows Installation Guide: https://graft.herominers.com/#windows



		cryptonote-proxy is a node.js program written by Seb Green that acts as a link between cryptonight mining software and the pool. Typically it is used by most users to quickly change pools without needing to restart their mining software. It can be used for any pool requiring the cryptonight algorithm (most cryptonote coins use this algorithm).
		

		
		A stratum-capable cryptonight mining software (eg. xmrstak, xmrig, cast-xmr etc.) is required to make use of cryptonote-proxy. When in doubt, any third-party mining software (i.e. not the one that came with your coin's daemon or wallet), is a stratum-capable miner.
		

	
		This guide is written with Debian/Ubuntu Linux in mind. However, it can be used for any Linux distro, by substituting the package manager-specific commands with the ones used by your distro.

		
		
		1. Download and install the latest nodejs version from <a target="_blank" href="https://nodejs.org/en/" title="NodeJs" alt="NodeJs" rel="nofollow">https://nodejs.org/en/</a>
		
  ![switch](https://images2.imgbox.com/70/56/iJhxsSJc_o.png)
		
		
		
				
	2. Download and install Git for Windows - <a target="_blank" title="git-scm" alt="git-scm" rel="nofollow" href="https://git-scm.com/download/win">https://git-scm.com/download/win</a>
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

		
	
		Save the config.json
	
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

  
  

Linux Installation Guide: https://graft.herominers.com/#linux



![switch](https://images2.imgbox.com/07/ce/H4UckRqP_o.png)
