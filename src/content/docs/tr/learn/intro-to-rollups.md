---
section: learn
date: Last Modified
title: "Rollup'lara Giriş"
lang: "tr"
permalink: "learn/intro-to-rollups"
excerpt: "Rolluplar, Ethereum ekosistemindeki en yaygın ikinci katman ölçekleme çözümüdür."
whatsnext: { "Scroll Rollup Süreci": "/tr/technology/chain/rollup" }
---

## Rollup nedir?

Rolluplar, Ethereum ekosistemindeki en yaygın ikinci kat ölçeklendirme çözümüdür ve Ethereum yol haritasının [merkezi bir parçası](https://ethereum-magicians.org/t/a-rollup-centric-ethereum-roadmap/4698) olarak görülmektedir.

Bir rollup, işlem gruplarını zincir dışında işler (yani katman 1'de değil) ve ardından ortaya çıkan verileri zincir üstünde yayınlar (yani katman 1'de).

Tüm işlemlerin yürütülmesi zincir-dışında gerçekleştirilir ve katman 1 düğümleri tarafından yeniden yürütülmesine gerek yoktur. Bu da, katman 1'in merkeziyetsizini etkilemeden yüksek işlem hızına olanak tanır.

Bir rollup'un güvenli olması için, zincir dışı hesaplamanın (işlemlerin işlenmesi) doğru bir şekilde gerçekleştirildiğini kanıtlaması gerekir. Zincir dışı hesaplamanın geçerliliğini kanıtlamanın iki temel mekanizması vardır: geçerlilik kanıtları(validity proofs) ve hile kanıtları(fraud proofs).

## Optimistic rollup nedir?

Bir optimistic rollup, yaptığı hesaplamaların geçerliliğini savunmak için hile kanıtlarını kullanan bir rollup'tır.

Hile kanıtları, kullanıcıların L2'de gerçekleştirilen herhangi bir hesaplamanın geçersizliğini sorgulamasına ve kanıtlamasına olanak tanıyan bir mekanizmadır. Bir hile kanıtı başarıyla gönderildiğinde, L2 bir önceki bir duruma geri döndürülebilir ve geçersiz hesaplama düzeltilebilir. Hile kanıtları, en az bir dürüst tarafın L2 işlemlerinin doğru bir şekilde yürütüldüğünü kontrol etmesine dayanır.

## ZK rollup nedir?

Bir ZK rollup, yaptığı hesaplamaların geçerliliğini savunmak için geçerlilik kanıtlarını kullanan bir rollup'tır.

When a ZK rollup executes a batch of transactions and posts the resulting state to L1, it also posts a validity proof. This mathematical proof proves that the resulting state is indeed the state which results from correctly executing the batch of transactions.
Bir ZK rollup bir işlem grubunu yürüttüğünde ve sonucu L1'e gönderdiğinde, aynı zamanda bir geçerlilik kanıtı da gönderir. Bu matematiksel kanıt, sonucun işlem grubunun doğru bir şekilde yürütülmesiyle ortaya çıkan durum ile gerçekten aynı olduğunu kanıtlar.

Today, there are multiple types of ZK rollups, broadly defined as either zkVMs (zk Virtual Machines) or zkEVMs (zk Ethereum Virtual Machines).
Bugünlerde birden çok türde ZK rollup bulunuyor, bunlar genel olarak zkVM'ler (zk Sanal Makineler) veya zkEVM'ler (zk Ethereum Sanal Makineleri) olarak tanımlanıyor.

zkVM'ler, ZK devreleriyle iyi çalışacak şekilde temelden tasarlanmıştır ve bir zkEVM'e kıyasla farklı geliştirme iş akışları gerektirir. Bunlara örnek olarak Starkware ve Aztec verilebilir.

zkEVM'ler, EVM'i taklit etmek üzere tasarlanmıştır. İki ana türü vardır: bytecode uyumlu ve dil uyumlu. Bytecode uyumlu zkEVM'ler, EVM'i çok düşük seviyede taklit eder ve Ethereum Katman 1'e kıyasla neredeyse aynı geliştirme ve kullanıcı deneyimi sağlar. Dil uyumlu zkEVM'ler, Solidity ve diğer yüksek seviye dilleri farklı bytecode'lere derler; bu da iş akışında değişikliklere neden olabilir. zkSync, en popüler dil uyumlu zkEVM'dir.

Scroll, bytecode uyumlu bir yapıya sahiptir. Bu yaklaşımın seçilmesinin bazı faydaları vardır:

- Solidity, Vyper ve Huff kutudan çıktığı gibi çalışıyor
- Yeniden kod denetimine gerek yok
- Varolan geliştirme araçlarının çoğu devralınır
- Ethereum ile neredeyse aynı kullanıcı deneyimi ve geliştirici deneyimi sağlar

Scroll'un yaklaşımına ilişkin daha fazla ayrıntı Teknoloji bölümünde bulunabilir.

## Daha fazla okumak için

- [Rollup'lar Hakkında Eksik Bir Kılavuz](https://vitalik.ca/general/2021/01/05/rollup.html) - Vitalik Buterin
- [Ölçeklenme](https://ethereum.org/en/developers/docs/scaling/) - Ethereum Dokümanları