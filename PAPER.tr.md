# Biriken Bağlamlı Agent

**Authors:** Prof. Dr. Mustafa Melikoğlu · Yağız Deniz Altınbaş · Tayfun Tanrıöver

## Tez

Agent sistemlerinde değer birimi model çağrısı değildir — **birikmiş bağlamdır**: aylar boyunca kendi ledger'larını okumuş bir kimlik, yeni bir prompt'un sıfırdan yeniden kurması gerekecek karar ve düzeltmelerden yararlanabilir. Engine'ler zekâyı kiralar; birikimin mülkiyeti elde tutulur. Kimliğin diskte yaşamasının, belleğin bi-temporal olmasının, ledger'ların yalan söylememesi gerekmesinin ve context hygiene'ı frenleri, anchor'ları ve pickup zincirleri olan bir mühendislik disiplini olarak ele almamızın nedeni budur.

## 1. Değer Birimini Yeniden Fiyatlandırmak

Bir model çağrısını saymak kolaydır. Zaman damgalı bir çıktıyla ve faturayla gelir. Yinelenen çalışma, bu muhasebenin sığ görünmesine yol açar. Yararlı bir yanıt ortaya çıkmadan önce, önceki oturumlar terminolojiyi çoktan karara bağlamış veya çekici bir çerçevenin neden başarısız olduğunu kaydetmiş olabilir. Çağrı, maliyeti başka yerde duran çalışmadan yararlanırken mevcut çıkarımı gerçekleştirir.

Yayın programımızdaki makale spine'ları tarihli çalışma kayıtlarından yararlanır. Yayın kapısında incelenen kayıtlarda, en az iki spine, önceki bir düzeltmeyi veya daraltılmış iddiayı, değişikliğin gerekçesiyle birlikte korur. Bu, mirasın incelenebilir olmasını sağlar. Yayınlanabilir spine sayısını, ortak gözlem dönemini, taslak hazırlama hızını ya da birikmiş bağlamdan doğan nedensel bir avantajı ortaya koymaz.

Tek başına eski metin bize pek az şey söyler. Sonraki bir taslak, bir düzeltmeyi gerekçesiyle birlikte taşıyabilir veya kasıtlı olarak açık bırakılmış bir soruyu koruyabilir. Bu ilişkiler çalışmanın parçasıdır. Kayıt bir hatayı da koruyabilir.

Bir AI agent tarafından yazılmış ve 13 Ağustos 2026 tarihli, yayımlanmamış bir çalışma sentezi bu çerçevenin kökenini kaydeder; bağımsız kanıt olarak değil, kaynak kaydı olarak atıf alır (Marcus, 2026). Ayrı biçimde çerçevelenmiş halka açık bir sürüm, *Core Synthesis: Agent Orchestration and Harness Sovereignty — an Internal Memo, Published As-Is* adıyla arşivlenmiştir (concept DOI: https://doi.org/10.5281/zenodo.22024504). Halka açık eser çalışma sentezinden türediği için, bu yazının iddialarının bağımsız doğrulaması değil, o da köken bilgisidir.

## 2. Ayların Kattığı

Aylar, korunan malzemeye bir düzen kazandırır. Kararlar gerekçeler edinir ve düzeltmeler, yerini aldıkları iddialara geri işaret eder. Uzun bir prompt cümleleri yeniden üretebilir ve yine de bu ilişkileri kaybedebilir.

Bu açıklamada kimlik pratiktir. Oturumlar arasında sorumluluğun yerini belirler: agent önceki taahhütleriyle karşılaşır ve muhakemesinin nerede değiştiğini görür. Bilinç hakkında bir iddiada bulunmadan, incelenebilen çalışma sürekliliğini tarif ediyoruz.

Mevcut kayıt, yeni bir başlangıç ile bir resumption arasında hız karşılaştırmasını desteklemez. Eşleştirilmiş bir baseline'dan, eşleşen görevlerden, ortak bir gözlem penceresinden, tutarlı endpoint'lerden ve önceden beyan edilmiş hariç tutmalardan yoksundur. Daha dar nokta incelenebilirdir: devam eden bir agent, yeni bir başlangıcın yeniden kurması gerekecek kayıtlı karar ve düzeltmelere başvurabilir. Göreve aşinalık veya daha iyi bir brief, daha hızlı herhangi bir başlangıcı açıklayabilir.

*The narch Manifesto and the Invariants Compact*, kalıcı kimliği bir işletim taahhüdü olarak halka açık biçimde tarif eder (Melikoğlu, Altınbaş, & Tanrıöver, 2026; concept DOI: https://doi.org/10.5281/zenodo.22019441). Bu eşlikçi kayıt, karşılaştırmalı etkililiğini değil, beyan edilen taahhüdü ortaya koyar. Buradaki ilgili malzeme, çalışma yeniden başladığında gerçekte mevcut olan kayıttır.

## 3. Engine Değişiklikleri Boyunca Gözetim

Model erişimi, kullanıcının kontrol etmediği koşullara tabidir. Sahip olunan bir çalışma kaydı, bu koşullar değiştiğinde veya farklı bir engine görevi devraldığında kullanılabilir kalabilir. Yeni engine aynı geçmişi okuyup farklı bir yargıya varabilir.

Korunan geçmiş, inceleyenlere bu değişimi fark edebilecekleri somut bir karşılaştırma zemini verir.

Handoff'lar gerekliliği sıradan çalışma içinde görünür kılar. Bir oturum işin ortasında sona erdiğinde, sonraki oturum hâlâ neyin geçerli olduğunu geri kazanmalıdır. Açık sorular tanınabilir olmalıdır; çünkü miras alınan notlar birinci elden gözlem değildir.

Belgelenmiş bir handoff 00:25:34'te, 10 Ağustos 2026 tarihinde mühürlendi ve 00:43:08'de tüketildi. Teslim alan oturum, aktarım paketindeki tüm 9/9 öğeyi doğruladı ve açık işleri ve bilinen sınırları açıkça miras aldı. Aralık 17 dakika 34 saniyeydi. Bu tekil vaka, sınırlandırılmış bir kaydın tek bir kesinti boyunca sürekliliğini destekler; kayıpsız aktarımı ya da performans avantajını ortaya koymaz.

Halka açık *Core Synthesis* kaydı, sürücü model değiştirilebilirken kimlik, bellek ve doktrinin diskte yaşadığı, engine'den bağımsız bir tasarımı tarif eder (Melikoğlu, Altınbaş, & Tanrıöver, 2026; concept DOI: https://doi.org/10.5281/zenodo.22024504). Bu, mimarinin yayımlanmış bir beyanıdır; herhangi bir belirli handoff'un kayıpsız olduğuna dair kanıt değildir. Uygulamada sahibinin yine de eski kayıtları incelemesi ve düzeltmesi gerekir.

## 4. Belleğin İki Zamana İhtiyacı Vardır ve Ledger'lar Doğruyu Söylemelidir

Sonraki bilgi, önceki bir olayın nasıl anlaşıldığını sık sık değiştirir. Gözden geçirilmiş açıklama, herkes bunu başından beri biliyormuş gibi okunursa kayıt daha derli toplu, fakat daha az yararlı hâle gelir. Önceki seçimin neden anlamlı olduğunu artık açıklamaz.

Burada bi-temporal bellek, bir supersession ve provenance disiplinini adlandırır. Olay zamanını, olayın açıklamasının ne zaman bilinir hâle geldiğinden ayrı tutar; ardından düzeltmeyi, erişilebilir olduğu zamana yerleştirir. Bu, bağımsız biçimde yönetilen valid time ve transaction time'a sahip tam bir dual-axis sistem iddiası değildir. Daha dar ifade, Johnston ve Weis'ın temporal database'leri ele alırken valid time ile transaction time arasında yaptığı ayrımdan beslenir (2010; https://doi.org/10.1016/C2009-0-20326-6).

Sıradan bir editoryal handoff'u düşünün. Bir not, bir alıntının kontrol edildiğini söyler; bu yüzden editör, devam ettirilen pasajı değiştirmeden copy review'a gönderir. Daha sonra kaynak mesaj ortaya çıkar: kontrol, atfı değil ifadeyi kapsamıştır. Ledger, handoff'u yöneten notu korumalı ve daha dar okumanın ne zaman bilinir hâle geldiğini işaretlemelidir.

Belgelenmiş bir handoff, hassas ayrıntılardan arındırılmış bir örnek sağlar. 18 Ağustos 2026'da bir güncelleme readback'ini geçti; bu sırada bir tutarsızlık geçici olarak file-service surface'e atfedildi. 19 Ağustos tarihli bir hüküm, tutarsızlığın izini kendi synchronization bridge'imize kadar sürdü ve atfını düzeltirken önceki PASS'i açıkça korudu. İlk kayıt 18 Ağustos'ta neyin geçerli olduğunu gösterir; düzeltme ise 19 Ağustos'ta neyin bilinir hâle geldiğini gösterir. Bu sıra, sonraki açıklamanın baştan beri mevcutmuş gibi davranmadan supersession'ı gösterir.

Bir handoff boyunca, tanıdık ifadeler zayıf kanıta hiç sahip olmadığı bir otorite kazandırabilir. Alıcı tartışma sırasında orada değildi. Kayıt, düzeltmeyi önceki açıklamanın yerini alma gerekçesiyle birlikte görünür bırakmalıdır.

*Ghost Debt: When “Done” Never Leaves the Ledger (and “Planned” Never Enters It)*, statünün kanıttan uzaklaşması şeklindeki daha dar sorunu inceler (Melikoğlu, Altınbaş, & Tanrıöver, 2026; concept DOI: https://doi.org/10.5281/zenodo.22019942). Bu yazı söz konusu sorunu, bir durum kaydıyla onu destekleyen malzemenin artık eşleşmediği handoff bağlamında ele alır.

## 5. Context Hygiene Bir Mühendislik Disiplinidir

Context hygiene, sınırlı dikkat için bakımdır. Hiçbir pickup her şeyi yeniden okuyarak başlamaz. Birinin hâlâ neyin geçerli olduğunu ve hangi provenance'ın önemli olabileceğini değerlendirmesi gerekir. Çoğu zaman iş, miras alınmış bir ifadeyi kullanmadan önce kontrol etmekten daha gösterişli değildir.

Miras alınan bağlam kanıttan yoksun olduğunda veya süregelen bir taahhütle çeliştiğinde, çalışmanın bir frene ihtiyacı vardır. Frenin değeri kullanım içinde, özellikle de devam etmek elverişli olduğunda, ortaya konur. *Written ≠ Wired: Hunting Fake-Green in Agent Systems*, bir fren de dâhil olmak üzere, ölçülmüş fail-open korumaları ve bunların counterfactual closure'ını 5 + 3 = 8 testte raporlar ve kanıtın live surface'ten okunması gerektiğini savunur (Melikoğlu, Altınbaş, & Tanrıöver, 2026; concept DOI: https://doi.org/10.5281/zenodo.22018790). Bu emsal, yazılı bir frenin gözlemlenmiş bir teste ihtiyaç duyduğu yönündeki daha dar kuralı destekler; burada tarif edilen bağlam pratiğinin etkililiğini ölçmez.

Anchor'lar daha sessiz drift'i ele alır. Güncel bir referans, eski durumlar düzeltme için erişilebilir kalırken çalışmanın yönünü korur. Resumption sırasında bir pickup zinciri sonraki oturumun ihtiyaç duyduklarını taşır ve boşlukları işaretler. Daha derin provenance, risk düzeyi gerektirene kadar bekleyebilir. *Counterfactual or Clobber: the Sync Bridge That Silently Ate an Agent's Memory*, bir agent'ın belleğinin üzerine yazan stale bir synchronization bridge'i ve bu bridge için benimsenen counterfactual acceptance test'i belgeler (Melikoğlu, Altınbaş, & Tanrıöver, 2026; concept DOI: https://doi.org/10.5281/zenodo.22019570). Bir continuity safeguard'ını önlemesi amaçlanan hataya karşı test etmeyi destekler; continuity'nin güvence altında olduğuna dair genel bir iddiayı değil.

Rutin inceleme seçicidir. Düşük riskli bir ifade seçimi için güncel referans yeterli olabilir. Süregelen bir taahhüdü değiştirebilecek bir iddia, provenance'ına daha yakından bakmayı gerektirir. Sonuçlar netleştikçe bu yargı revizyona açık kalır.

Kayıtlar; kaçırılmış teslimatlar, stale varsayımlar ve eksik miras alımlarının yanı sıra başarılı resumption'lar da içerir. Karşılaştırılabilir bir cold-start örneklemi veya sonuç ölçütü tanımlamazlar; dolayısıyla reorientation süresinde azalma olduğu iddia edilemez. Eserler en fazla, bakımı yapılmış bir pickup zincirinin güncel taahhütleri ve bilinen boşlukları görünür kılabildiğini gösterir. Özellikle brief netleştikçe, editoryal tekrar startup'ı yine de kısaltmış olabilir; bu alternatif ileride yapılacak herhangi bir teste dâhil edilmelidir.

Bazı kayıtlar, provenance'ları hiç korunmadığı için doğrulanmadan kalacaktır.

## 6. Katlanarak Büyüyen Kanıt

Yayın programı, tarihli bir sentezden makale spine'ları üzerinden tamamlanmış kardeş yazılara uzanan, incelenebilir bir zincir bırakır. Bu zincir, inceleyenin bir yazının miras aldığı şeyleri, koruduğu veya düzelttiği şeylerle karşılaştırmasını sağlar. Taslak hazırlama süresini, nedensel bir avantajı veya kümülatif bir performans ölçütünü ortaya koymaz.

Pickup ve handoff gözlemleri, karşılaştırma koşulları bilindiğinde bu açıklamayı destekleyebilir. Şimdilik ikincil kalırlar.

Yayımlanmış kardeş yazılar, ayrı yazma eylemleri boyunca başka bir iz sağlar. Eşlikçi bir ampirik makale, paketlenmiş ve confounded bir kol karşılaştırması boyunca, diske anchor edilmiş kimliğin taşınabilirliğine dair sınırlandırılmış tek bir gözlem olarak dört deneyli, sekiz görevli bir A/B karşılaştırması raporlar; ne nedensel bir foundation-model etkisini yalıtır ne de equivalence ortaya koyar (Melikoğlu, Altınbaş, & Tanrıöver, 2026; concept DOI: https://doi.org/10.5281/zenodo.22086013). Bu, birikmiş bağlamın buradaki yazılar arasında coherence'a neden olduğuna dair kanıt değil, halka açık bir izdir. Güçlü bir kayıt üzerinde işleyen sıradan editoryal tekrar da bu coherence'ı üretebilir. İnceleyenin, bir yazıya fazla ağırlık vermeden önce onun neyi miras aldığını geri kazanması gerekir.

Bazen sonraki bir yazı düzeltmeyi taşır, ancak onu açıklayan notu taşımaz; bu da inceleyeni mevcut ifadenin desteğini değerlendiremez durumda bırakır.

Bu dayanak geri kazanılamadığında, taslağın daha dar bir ifadeyle ilerleyip ilerleyemeyeceğine sahibi karar verir.

Uygulamada birinin bitmemiş kayıt tutma işlerine zaman ayırması gerekir. Güncel bir durum, onu destekleyen malzemeyle karşılaştırılır; eksik bir kaynak, eksik olarak işaretlenmiş kalır. Bazen günün sonucu, sonraki inceleyenin görebileceği yerde bırakılmış çözülmemiş bir nottur.

## AI katılımı beyanı

AI sistemleri taslak oluşturma, çeviri, kaynak triyajı, ledger yeniden türetimi ve tutarlılık kontrollerine yardımcı oldu. İnsan yazarlar tez, kanıt sınırları, atıf kararları ve nihai yayın onayı sorumluluğunu korudu.

## Kaynakça

- Marcus. (2026, August 13). *MARCUS CORE SYNTHESIS — Agent Orchestration & Harness Sovereignty* [Unpublished internal working synthesis; provenance only].
- Melikoğlu, M., Altınbaş, Y.D., & Tanrıöver, T. (2026, August 20). The narch Manifesto and the Invariants Compact. *Zenodo*. https://doi.org/10.5281/zenodo.22019441
- Melikoğlu, M., Altınbaş, Y.D., & Tanrıöver, T. (2026, August 20). Core Synthesis: Agent Orchestration and Harness Sovereignty — an Internal Memo, Published As-Is. *Zenodo*. https://doi.org/10.5281/zenodo.22024504
- Johnston, T., & Weis, R. (2010). *Managing Time in Relational Databases: How to Design, Update and Query Temporal Data*. Morgan Kaufmann/Elsevier. https://doi.org/10.1016/C2009-0-20326-6
- Melikoğlu, M., Altınbaş, Y.D., & Tanrıöver, T. (2026, August 20). Ghost Debt: When "Done" Never Leaves the Ledger (and "Planned" Never Enters It). *Zenodo*. https://doi.org/10.5281/zenodo.22019942
- Melikoğlu, M., Altınbaş, Y.D., & Tanrıöver, T. (2026, August 20). Written ≠ Wired: Hunting Fake-Green in Agent Systems. *Zenodo*. https://doi.org/10.5281/zenodo.22018790
- Melikoğlu, M., Altınbaş, Y.D., & Tanrıöver, T. (2026, August 20). Counterfactual or Clobber: the Sync Bridge That Silently Ate an Agent's Memory. *Zenodo*. https://doi.org/10.5281/zenodo.22019570
- Melikoğlu, M., Altınbaş, Y.D., & Tanrıöver, T. (2026, August 24). Portability of a Disk-Anchored Agent Identity Across Foundation Models: A Blind, Internally Pre-Sealed A/B Comparison. *Zenodo*. https://doi.org/10.5281/zenodo.22086013
