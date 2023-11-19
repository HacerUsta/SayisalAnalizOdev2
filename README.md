# SayisalAnalizOdev2
#Hacer Usta 02220224005

#SORU1
aralik_1=2
aralik_2=4
i=0#düzgün print çıktısı için sayac görevi görüyor
print("SORU1")
for i in range(4):
    ortanca = (aralik_1 + aralik_2) / 2
    f_1 = aralik_1 * aralik_1 * aralik_1 - 2 * aralik_1 * aralik_1 - 5
    f_2 = aralik_2 * aralik_2 * aralik_2 - 2 * aralik_2 * aralik_2 - 5
    f_3 = ortanca * ortanca * ortanca - 2 * ortanca * ortanca - 5
    if (f_1 * f_3)<0:
        aralik_2=ortanca
        f_2=f_3
    else :
        aralik_1=ortanca
        f_1=f_3
    i=i+1
    print(i,".iterasyonu=","[",aralik_1,",",aralik_2,"]=","[",f_1,",",f_2,"]")
print(ortanca,"=",f_3)

#SORU2
print("\nSORU2")
aralik_1=1
aralik_2=2
sonuc=1
sayac=1
us=1
while sonuc>0.000001:
    ortanca = (aralik_1 + aralik_2) / 2
    f_1 = aralik_1 * aralik_1 * aralik_1 + 4 * aralik_1 * aralik_1 - 10
    f_2 = aralik_2 * aralik_2 * aralik_2 + 4 * aralik_2 * aralik_2 - 10
    f_3 = ortanca * ortanca * ortanca + 4 * ortanca * ortanca - 10
    b = aralik_2
    a = aralik_1

    if (f_1 * f_3)<0:
        aralik_2=ortanca
        f_2 = f_3
    else:
        aralik_1 = ortanca
        f_1 = f_3
    us*=2
    sonuc = (b-a)/us
    sayac+=1
print(sonuc)
