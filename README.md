# turkish-image-captioning

Bu alan Görüntü Altyazılama  için Otomatik Tercümeyle Eğitim Kümesi Oluşturulabilir mi? (Could We Create A Training Set For Image Captioning Using Automatic Translation? ) başlıklı makaleye ait kodları ve kullanılan Türkçe altyazıları içermektedir. 

[IEEE](https://ieeexplore.ieee.org/abstract/document/7960638)
[PDF](http://users.metu.edu.tr/e213461/papers/siu2017.pdf)

## Veri Setleri

### Flickr30k

[Flickr30k](Flickr30k/train): Flickr30k veri setine ait Turkce altyazilar. 
NOT: Burada model egitilirken TasvirEt altyazilarina ait imgeler ve altyazilari kullanilmamalidir. Cunku Flickr30k veri seti, Flickr8k veri setindeki imgeleri ve altyazilari icermektedir. Bu duruma dikkat edilmelidir.  

### COCO

[MSCOCO](MSCOCO): MSCOCO veri setine ait Turkce altyazilar. 

[Egitme](MSCOCO/train): MSCOCO veri setinin egitme kumesinin Turkce altyazilari. 

[Dogrulama](MSCOCO/val): MSCOCO veri setini dogrulamak icin MSCOCO Validasyon setindeki 500 imge 2 kisi tarafindan el ile altyazilanmistir. 

[Kullanilan Imgeler](MSCOCO/val/val_file_names.txt) sunlardir. Her imgeye ait 2 farkli kisi tarafindan uretilen dogrulama altyazilari 1 ve 2 uzantilari ile verilmistir. .json uzantili dosyalar metrik hesaplanirken kullanilan sisteme uygun haldedir. Ayni zamanda zemberekten gecirilmis halleri de mevcuttur.

Burada sonuc metriklerini hesaplamak icin [Microsoft COCO Caption Evaluation code](https://github.com/tylin/coco-caption) kullanilmistir.

Modeli egitirken [NeuralTalk2](https://github.com/karpathy/neuraltalk2) kodu kullanildi. Test adiminda -dump_path secenegi aktif edilmelidir. Bu sayede dosya isimleri 1.jpg, 2.jpg gibi degil, orijinal isimleri ile kullanilabilecektir. Metrikler hesaplanirken imge dosyalarinin tam isimleri gerekmektedir.


## Model Dosyalari: 

Flickr icin en iyi basarim veren model dosyasi:

[Dropbox](https://www.dropbox.com/s/8xrwwjixhnm9s0l/model_flickr30k_tr.t7?dl=0)

MSCOCO icin en iyi basarim veren model dosyasi:

[Drive](https://drive.google.com/file/d/1K8ZpvS09PQCfrmOoLzjiJTRDMoEUT7jD/view?usp=sharing)
