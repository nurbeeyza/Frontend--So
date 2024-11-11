## İsimlendirme Kuralları ve Öneriler

Bu projede çalışırken uygun isimlendirme kurallarını ve en iyi uygulamaları takip etmek önemlidir. Bu, temiz ve okunabilir bir kod oluşturmamıza yardımcı olacaktır. Ayrıca yanlış isimlendirme kurallarından kaynaklanan merge conflict ve diğer sorunları önlemeye yardımcı olur.

### İsimlendirme Kuralları ve Bir Ticket'ı Tamamlama Yöntemi

Bir ticket üzerinde çalışırken, ilk olarak `master` branch'inden en son değişikliklere sahip olduğunuzdan emin olmalısınız. Bunu yapmak için aşağıdaki komutları çalıştırın:

```
git checkout master
git pull origin master
```

`master` branch'inden en son değişiklikleri çektikten sonra, ticket'ınız üzerinde çalışmak için yeni bir branch oluşturabilirsiniz. Yeni bir branch oluşturmak için şu komutu çalıştırın:

```
git checkout -b <branch-ismi>
```

`<branch-ismi>` şu formatta olmalıdır:

```
<adınız>/<ticket-numarası>-<ticket-başlığı-veya-açıklaması>
```

Örneğin, `CO-120` numaralı ticket üzerinde çalışıyorsanız ve adınız `John Doe` ise, branch isminiz şöyle olmalıdır:

```
johnDoe/CO-120-hero-section
```

Branch oluşturduktan sonra ticket'ınız üzerinde çalışmaya başlayabilirsiniz. İşiniz bittiğinde, değişikliklerinizi remote repository'ye gönderebilirsiniz. Bunu yapmak için şu komutları çalıştırın:

```
git add .
git commit -m "[<ticket-numarası>] - <commit-mesajı>"
```

Örneğin, `OC-120` numaralı ticket üzerinde çalışıyorsanız ve hero section için HTML markup uyguladıysanız, commit mesajınız şöyle olmalıdır:

```
git commit -m "[OC-120] - HTML markup uygulandı"
```

Commit ettikten sonra, değişikliklerinizi remote repository'ye gönderebilirsiniz. Bunu yapmak için şu komutu çalıştırın:

```
git push origin <branch-ismi>
```

Örneğin, branch isminiz `johnDoe/OC-120-hero-section` ise, şu komutu çalıştırmalısınız:

```
git push origin johnDoe/OC-120-hero-section
```

Değişikliklerinizi gönderdikten sonra, bir pull request oluşturabilirsiniz. Bunu yapmak için [repository'e](https://github.com/archis-academy/coral-buy-feb-2024) gidip `Pull requests` sekmesine tıklayın. Sonra `New pull request` butonuna tıklayın. `base` branch'in `master` ve `compare` branch'in `<branch-ismi>` olduğundan emin olun. Pull request başlığı şu formatta olmalıdır:

```
[<ticket-numarası>] - <ticket-başlığı-veya-açıklaması>
```

Örneğin, `OC-120` numaralı ticket üzerinde çalışıyorsanız ve hero section için HTML markup uyguladıysanız, pull request başlığınız şöyle olmalıdır:

```
[OC-120] - Hero section için HTML markup
```

Kendinizi assign edin ve takım arkadaşlarınızı ve takım liderinizi reviewer olarak ekleyin. Ardından `Create pull request` butonuna tıklayın ve `Lokum` ticket'ınızı pull request linki ile güncelleyin.

![Assign reviewers to the ticket](https://user-images.githubusercontent.com/71005514/284887977-9bece5e1-ee6b-4ffb-b098-d093ee31a52d.png)

### Tavsiyeler

- Tüm görevi tamamlamayı beklemeden bir commit yapın. Görevinizi daha küçük parçalara ayırın ve her bir parça tamamlandığında commit yapın.

---

## GEREKSİNİMLER

Aşağıdaki kursları tamamlamış olmanız gerekmektedir:

- Frontend Development - Beginner
- Learn Git With Zero Coding Knowledge
- Web Development Basics
