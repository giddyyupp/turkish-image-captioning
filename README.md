# turkish-image-captioning

Bu alan Görüntü Altyazılama  için Otomatik Tercümeyle Eğitim Kümesi Oluşturulabilir mi? (Could We Create A Training Set For Image Captioning Using Automatic Translation? ) başlıklı makaleye ait kodları ve kullanılan Türkçe altyazıları içermektedir (içerecektir). 

[Flickr30k](Flickr30k/train): Flickr30k veri setine ait Turkce altyazilar.
[MSCOCO](MSCOCO): MSCOCO veri setine ait Turkce altyazilar. 

Burada sonuc metriklerini hesaplamak icin [Microsoft COCO Caption Evaluation code](https://github.com/tylin/coco-caption) kullanilmistir.


Modeli egitirken [NeuralTalk2](https://github.com/karpathy/neuraltalk2) kodu kullanildi. Test adiminda -dump_path secenegi aktif edilmelidir. Bu sayede dosya isimleri 1.jpg, 2.jpg gibi degil, orijinal isimleri ile kullanilabilecektir. Metrikler hesaplanirken imge dosyalarinin tam isimleri gerekmektedir.

[Create Baseline](flickr30k_create_baseline_json.py):
searches test files using Flickr8k test image names. And creates a baseline json file.

[Create Test](flickr30k_create_result_json.py):
creates result json using vis.json file 
