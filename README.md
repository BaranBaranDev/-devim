def tasit():

    dizelSayisi = 0
    benzinSayisi = 0
    otogazSayisi = 0
    dizelGider = 0
    benzinGider = 0
    otogazGider = 0
    toplamTasit = 0
    
    

    while True:

        ekleme = input("\nEklemek ister misiniz? (e/h): ") 
        if ekleme == "e":

            motorTipi= input("Motor tipini giriniz (x: benzin, y: dizel, z: otogaz): ")
            yakıtGider = int(input("Aylık yakıt giderini giriniz (TL): "))

            if motorTipi == "x":
                benzinSayisi += 1
                benzinGider += yakıtGider
                toplamTasit += 1
            
            elif motorTipi == "y":
                dizelSayisi += 1
                dizelGider += yakıtGider
                toplamTasit += 1

            elif motorTipi == "z":
                otogazSayisi += 1
                otogazGider += yakıtGider
                toplamTasit += 1

            elif motorTipi == "q":
                print("Çıkıldı")
                break
            
            else:
                print("Hatali tuslama yaptiniz. Tekrar deneyiniz.")

        elif ekleme == "h":
            toplamGider = dizelGider + benzinGider + otogazGider
            if toplamGider != 0 and toplamTasit != 0:
                tasitOrtalamaGider = toplamGider / toplamTasit
            else:
                tasitOrtalamaGider = "Hesaplanması için değer ekleyin."
            print("\nSONUÇLAR\n")
            print(f"Taşıt sayıları;\nDizel taşıt sayısı: {dizelSayisi}\nBenzinli taşıt sayısı: {benzinSayisi}\nOtogazlı araç sayısı: {otogazSayisi}")
            print(f"\nTaşıt aylık toplam giderleri;\nDizel taşıt toplam gideri: {dizelGider}\nBenzinli taşıt toplam gideri: {benzinGider}\nOtogazlı araç toplam gideri: {otogazGider}")
            print(f"\nToplam taşıt sayısı ve gideri;\nToplam taşıt: {toplamTasit}\nToplam gider: {toplamGider}")
            print(f"\nBir taşıtın gideri;\nBir taşıtın ortalama yakıt gideri: {tasitOrtalamaGider}")
            break

        else:
            print("Hatalı tuşlama yaptınız. Tekrar deneyiniz.")

tasit()





