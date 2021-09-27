  Public Key Cryptography
=======================

   Public key cryptography is powerful in general because it is one of the few things on the planet that can create an [asymmetric power](https://searchsecurity.techtarget.com/definition/asymmetric-cryptography){target=_blank} imbalance. This means that, even if the largest corporation or government were to focus every available resource into figuring out a certain individual's private key, they will not be able to do it. Isn't that crazy!? This asymmetric power imbalance is so dramatic that in the 1990s, world governments fought against the use of public key cryptography. The argument was, because public key cryptography essentially cannot be broken, it represented a critical threat to the national security of governments like the United States. We'll discuss this history more in a following section, but know that at one point using this technology was almost illegal! 

  Public key cryptography is powerful for blockchain specifically because it allows us to prove a message has been sent from a certain person holding a specific private key. This is a step in the direction of establishing identity in a peer-to-peer way. Remember, a blockchain protocol is trying to provide what banks or governments have previously provided but without those institutions as intermediaries. What public key cryptography does is mathematically prove a certain person holds a certain key. 

 Consequences
------------

  However, there's a big issue here. There's no way to determine who holds the key, just if they have the key. We are assuming the private key equals the owner of the assets, but what if someone steals your private key? This is a big security and user-experience issue for people coming into the blockchain and cryptocurrency world. 

  As consumers, users are probably used to being able to reset their passwords, recover their funds if there's fraud, or at least reach out to a service and get assistance in case of trouble. At its most basic, with users handling their own private keys, almost all of this disappears. 

  Even more troubling, regardless of the amount of messaging a user receives about protecting their private keys, many may not understand there is no safety net until it is too late. And for those users who are experienced, there are so many bad habits we've all developed as consumers which are hard to break. 

  All this to say: [Not trusting is expensive.](https://twitter.com/danfinlay/status/1386474006937706496){target=_blank} Please be aware of how expensive it is, not only for yourself, but also for your users. Luckily, at the end of this section, we'll walk through some basic security considerations that **anyone** in the crypto space should adopt from Day 1 

 Okay! Parental lecture over, stepping off of soapbox, and now time to play with some public keys cryptography!

 Moar on Keys
------------

 ![private all the keys meme, x all the y meme template](../../../img/S01/private-all-the-keys.jpeg) There are a ton of additional resources for public key cryptography, so we're going to break them up into different sections: **General Public Key Cryptography Resources**, **Blockchain / Ethereum-Specific Public Key Cryptography Resources** and **Advanced Public Key Cryptography Resources**.

 ### General Public Key Cryptography Resources

 Know that in these examples, you will meet some lifetime friends, Alice and Bob. They are the most absolutely unimaginatively, Eurocentric named parties in every cryptographic key exchange (rather than using A and B). Please, *please* if you're ever teaching this to someone else use a more interesting name than Alice and Bob, like Akash and Basilia. But, it is the common way to discuss it and perhaps there's value in that commonality across cultures.

 * [Video & Interactive Code: ETH.Building with Key Pairs](https://youtu.be/9LtBDy67Tho){target=_blank} Excellent hands-on tutorial about public keypairs from Austin Griffith using his [ETH.Build platform](https://sandbox.eth.build/wofCrGxhc3Rfbm9kZV9pZMONAQ_EgcSDxIVsaW5rxItkw4zDrsKlxIfEiXPCnsKKwqLEjMOMw73CpHR5cGXCrElucHV0L0LEr3RvbsKjcG9zwpJ1xI4NwqRzaXplwpLDjMOIMsKlZsSCZ3PCgMKlb3LEiXIAwqRtxIhlAMKmxJXErnRzwpHCg8KkbmFtZcKgxKbEqGXDv8KkxJTElsOAwqdvxK_Fm8S6xZ_FocWjxaXEp8Spw7_CpcWra8Wdw4zDmsWzxaLFpMWmxKnCrm51bWJlcixib29sZWFuxbrElcW8w4DCqnByb8SpcnRpZXPCg8KldmFsdWXCqGPElGNrIMWjwqXGnnTGkMKmxLJ0xLTGk2PFr250AMShxIzEjgHGg2XCrURpc3DEgnkvV2F0Y2jEt8S5wpLDjQLCnsOMwrTEv8WBxYPHlBE8xYjFisWMxY7FkMaKBsWUxZbFmMWaxK_FncKExaDGgcW2xafFk8W7w4zDnsW6YcaJbMKgxa7FsMeqwpHHrMW0xoLFt8WXxpTElnPDgMe1x7fCoMaYxprGnMaexqDCgcawacayZcKlx4zHjmjCicSixI0BAseCwq_HhceHx4kvQWRkcsagc8eRxLrDjQUKw4zCqseZxYLHkwFWT8efYcWLxY3Fj8WRB8emxInHqMStx7zGgMW1x4LHscaVw4zDn8iKxpvGisiNc8KEwqtibG_GrMafU8eaMsKrx4hhY2Voxo_FkcKgyJDIksKnyKPIpcinxqPGpcanw5kqMHgzMmE5ZTkxOWNmODJkybY4ZDUwMjRlMcqCMGE1M2IwMzU1ybJlNGZixr7ImselyIHHhMeGyZnHisiVx4_IqceTAsKUxI7DoMiwx5sGSceexYnIt8ehyLrGigjIvcWXxZnJgMWcx73HrcmDyIHJhcSWw4zDo8iHZce4x7p0xbHKs8e_x6_EqQDIg8aWyrvHuMmJyIzGn3PIj8axxpDIlMeNx4_Kk8SOyLzIgcKuQ3LEqMS0L1Jlxrl2xorKnceUCMeUw7jKo8KCwqEww4pDITMzwqExLsi2yLjHosWRCcquyL_FscKSyYJlwqlbxaNzc8i3ZV3HgsKmxIRyxJVnxarJhsOpy73Cq1vFgGfFoXR1yKbMhsiBzIh0zIpuzIzHssOoyr7LgMu9wqdhyKTIpsyCzIfMicyLy4bEusOMw6bDjMOny4rJi8uMwoLCp8yBzINnZcK9dGhlIMaJYXIgx4YgxIRpxqx5IHfIkWggyZ1uZXnCqcyTzJXMl2XDmcKEyaw4NzVkMjBlYsqAZsuvNTlmyKTNnDLNp8uvMjM4NDk5NGEyzbM3NzEyODbNt2Mwzac2YjkwMTPEic27ZDFiZsqKMc2xzok0zoY3YTfNt2TKiMqQNsm4M82oxok4Nc6Nzb1jNzY5OMm_Y86AMmY3ZGE2zafJvc2izbTOpcm5MWE4zozLlAEDx4LCq8uZy5tvL8mVzJTLowHCrsqhy6jLqsusOmZmy7FWy7TKqsejcgTLucqwxbHClMu9wqxbxplpxqR0ZWvNksyZxafMm8ydzJ_JhsOgy73Cqs-fxpp2xIzGis-nxKnPqcyLzI3FrMu9y7_MuMyEz7Vlz7fMns-5a8OMw6HLvceZzJTHgsWpxbvFrcWvyr_Hqs-cyrRlzKXMp8inzKrMnMysxbvIhcykz73MutCXz6rMrcOAz7vNlceNzZfQn9CZxpXMrsOjw4zDqMu9zIhpzJRlZNCK0KHMs8ady4zChcy3yKfMhMy8zL7NgMaRzYPNhc2HzYnNi82NzY_Etc2SyIrPoceNZUvNksOZQsmszbo3zq5jOM2iybjNvmZhzobNocqJzqg5ya9izqdjzbbNsGXOp829N2LOi86uzbtmMTY2zKbOpjLNucm4NTTNusKoxplvz7LFkcK6aMa2cHM6Ly9hdc2HzJ7Mis-QzY0uxrltzZTQsM2WyKbDgMKo0onEtM-GbsODzr0Kx4LKl8igYcqay5LHkMS4yKoDIMeUwp7Ko8qex53PlMi5z5YLz5nHqcqyx77HrsmE0IPMr8uIx7nQjsuA0rfKtcew0KHSvNC2yYzLjsiRy5DKm8iXyJnEjtKzyIHInsqYyKHJpMyoyKjSp8eTAyrDjQM00q3EjkBQ0rDLtsaKDNK0yrHFncu9y4PFl9K6zLLRvcuLxqDJjsmQyZJryZTJlsmYxILJm8mdbMmfyaHGkMmj0JXMgsmnxqbNmMmrya3Jr8mxybPJtcm3ybnJu8m9yb_KgcqDMcqFyofKicqLyo3JscqQYsKI04wB06TKlsifypkvVNOIZcqdUFrTnQHDtMuFyqjLtcqrcseBxZXIvtOFy4zCh8KoZsS1dMmVxYIsyY_JkcmTZdS6ZcmXyZnTuMmexorJoMuPyJPUosiS1IHGp8Ko0Y7NilBhaXLCqtS3xrtGxaJpbHnCvCdSdWJpxq1NxLVvIE_NkScszYbGknMtc8aKaWbCpca5yZFywqcjyKTVu2TOvc-YyIHCqsSsxZvUoWV4dNSlxI7DqtSoLMWH1KzPlcWRyJzUscqv0rXTp9CS06nKt2vQjce7yrLTqNCnzJ7MrcKT0IXDjMOpw4zDq9Sz06_UvdOy07TFgtWD07fJnNWGcsKvZca7xoogz6PWhs2PxorIk9WJwqRU1oV01Y3Mu8y9zL_NgdGBc82Gxp7RhM2MzL3Rh82RecqTw4zDvMidz4Jwy5zVkCDVktWUz4jCg8OMw5vPjMurQ1PCmcKay7FC06HUrs6_1pLLuseqy7zQksKtz7DRi8-jIM-lec-_0IHPq8-60JLCqMy6zZFy0YzQitK6w5rMoseqwpPMkM-gz6LMv9e01p5nzK3FhMOgxJrPrsSuyZDNiNezzZLYi8ytwpHDjMOqzKTMpsmlzKnMmsyr1p_QmsWEw57Jh9any43RitiI1ZDRkM2bN82xZc6pZsmvzqHNqWLKiDA0zqvRrM23Nc27zaEwzrfVgmPNtM2dybjGidSU2LDNndi5Mc6zN2XNp9GWzr0Ox4LLmMua15XPhETLn9mW1ofTlseUworDjQTHpcWAyLHHly3Xp8-W0p_Xqs-a16zYhsyK2IjYlXnYi9K6w67Pu9azY9mb0LLZsseyw6zYg9ac0JLCqcSJ2bfLm9m5zJpvYmrLn9eA0JrYmcOt2KfCgM69xL7Ll9eUy5xFbtqC15XPiHLZoNmix5rFhMK02abWjtKxxZEF06XLu9iR1aHGq9mw2brJhtib0JLQusyCzITaq8q4w6vZvcWy0JLCptqG2ohjdMyH2rnaidCh2bXaltm40LPYoNCY2KLQqdiZw6zajs69D9Kg1J_IodOKy6MDwo7am9Sodcqnx6DaosaKxL7ZqtaUy4HSuMq20rrDrdK82rXbn9OBy4TTg8SCyIjYp9OH1YzTisytwp_ClsW-xKQA15EBw7_bstilw7wCx4AAANuyw5_Xkdu8yJvbvtuy2I_DvADEjgPFmNihZ9uyw6HEjgTcic6-Ate327LDo9yK3IMG3IXMr8uV3JMK3JzDp9ye043cnMOo3JnLlQHcltaj3JHckwfcjNuG3I7Ymtu2xL3cr8-q27LDq9ysxL3cqdyN27LDrNy6xI4O3LvcsNuyw63dgNyTD9ycw67XkdyTDty1zIvCpmfGmnXShMKQwqbGuW5m0LDCgMKny6FyxYDEtcOLP8OZwpndpN2kwpo){target=_blank} (highly recommended)
* [Article: Public Key Cryptography (Wikipedia)](https://en.wikipedia.org/wiki/Public-key_cryptography){target=_blank} A good starting place for folks to get an understanding of the terms and be able to dig into some of the background or deeper ideas.
* [Video: End to End Encryption — Computerphile](https://www.youtube.com/watch?v=jkV1KEJGKRA){target=_blank} Introducing the general concepts behind using encryption in public networks
* [Video: Gambling with Secrets — RSA Encryption](https://www.youtube.com/watch?v=vgTtHV04xRI){target=_blank}
* [Article: What is Asymmetric Encryption?](https://dzone.com/articles/what-is-asymmetric-encryption-understand-with-simp-1){target=_blank}
* [Article: Keeping Secrets Secret (BBC)](https://www.rigb.org/christmaslectures08/html/activities/keeping-secrets-secret.pdf#page=5){target=_blank} This is a valuable resource explaining, in simple visual terms, the modular arithmetic underpinning the security of public key cryptography, hashing (which we'll learn about next) and any other one-way or "trapdoor" functions. It illustrates how you cannot break a private key's encryption with brute-force but can easily validate it if you have the accompanying public key.
* [Video: Secret Key Exchange — Computerphile](https://www.youtube.com/watch?v=NmM9HA2MQGI){target=_blank} Not public key encryption but good to know in terms of general cryptography mechanics
* [Video: Elliptic Curves — Computerphile](https://www.youtube.com/watch?v=NF1pwjL9-DE){target=_blank} Going deeper into the Elliptic Curve encryption behind public key cryptography.
* [Mini-Course: Basic Key Exchange](https://www.coursera.org/learn/crypto/home/week/5){target=_blank} Requires a free Coursera registration, but this is another general overview on the mechanics of key exchanges (not RSA encryption specifically) from Dan Boneh's [Cryptography I course](https://www.coursera.org/learn/crypto){target=_blank} from Stanford University.

 ### Blockchain / Ethereum-Specific Public Key Cryptography Resources

 Now that you have an understanding of public key cryptography generally, let's dive into how it is used in blockchains, specifically Ethereum. The following links will mainly show how private keys are used to generate Ethereum accounts, which then become a stand-in for identity on the Ethereum network. Note that all Ethereum addresses start with the first two characters `0x`, which is not actually part of the address but rather a prefix used to let programs know the address is coded in hexadecimal format.

 * [Book Excerpt: Keys and Addresses (Mastering Ethereum)](https://github.com/ethereumbook/ethereumbook/blob/develop/04keys-addresses.asciidoc){target=_blank} Excerpt from Andreas Antonopoulos and Gavin Wood's excellent book, *Mastering Ethereum* available for free as an e-book through [this GitHub repo.](https://github.com/ethereumbook/ethereumbook){target=_blank}
* [Article: How are Ethereum Addresses Generated? (Stack Overflow)](https://ethereum.stackexchange.com/questions/3542/how-are-ethereum-addresses-generated){target=_blank} A nice, thorough answer walking through the process of generating a private key to having an Ethereum address linked to that private key

 ### Advanced Public Key Cryptography Resources

 * [Coding Problem Set: Cryptopals](https://cryptopals.com/){target=_blank} This is an extremely advanced problem set series discussing applied cryptography generally. Not for the faint of heart!

 