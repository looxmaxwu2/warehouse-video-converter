# Basit Video WebM Dönüştürücü

Bu proje, web tarayıcısı üzerinde çalışan basit ve modern bir video dönüştürme uygulamasıdır.  
Kullanıcıların bilgisayarlarından yükledikleri videoları **WebM** formatına dönüştürmelerine olanak sağlar.  

## Özellikler

- Tamamen tarayıcıda çalışır, herhangi bir sunucuya ihtiyaç yoktur.
- Video dosyasını WebM formatına dönüştürür (codec: VP8).
- Dönüştürme işlemi bittikten sonra videoyu önizleme ve indirme imkanı.
- Basit, şık ve kullanıcı dostu arayüz.
- GitHub Pages ve benzeri statik site barındırma servislerinde kolayca çalışır.

## Kullanım

1. `input` butonundan video dosyanızı seçin.
2. **Videoyu WebM'ye Dönüştür** butonuna tıklayın.
3. İşlem tamamlandığında videonun önizlemesini görebilir ve **Videoyu İndir** butonuyla dönüştürülmüş dosyayı indirebilirsiniz.

## Sınırlamalar

- Sadece WebM formatı desteklenir (tarayıcı ve MediaRecorder API kısıtlamaları nedeniyle).
- Büyük videolarda dönüştürme işlemi uzun sürebilir.
- Tarayıcınızın `MediaRecorder` API desteği gereklidir (modern Chrome ve Firefox önerilir).

## Neden ffmpeg.wasm kullanmadık?

GitHub Pages, WebAssembly ve özellikle `SharedArrayBuffer` için gereken güvenlik başlıklarını (COOP/COEP) desteklemediğinden, ffmpeg.wasm tabanlı video dönüştürme çalışmamaktadır.  
Bu yüzden sadece tarayıcı içi `MediaRecorder` API'si kullanılmıştır.

## Geliştirme ve Katkı

- Yeni formatlar ve özellikler eklenebilir.
- Kullanıcı arayüzü geliştirilebilir.
- Farklı barındırma ortamlarında (Netlify, Vercel vb.) ffmpeg.wasm entegrasyonu yapılabilir.

## Lisans

MIT License

---

> Basit ve hızlı video dönüştürme ihtiyaçlarınız için ideal, tamamen client-side çalışan bir çözümdür.

