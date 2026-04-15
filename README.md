# securite-mobile-lab19x

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d16b2f8f-e5b8-4918-90f4-9949d7be8ae4" />


<img width="996" height="340" alt="image" src="https://github.com/user-attachments/assets/bbf03f51-37ec-4e97-8d50-c8c1767d5117" />
<img width="900" height="862" alt="image" src="https://github.com/user-attachments/assets/aefa4fef-3a39-4c8b-8f79-aad6bd5bf3ab" />
<img width="1281" height="1000" alt="image" src="https://github.com/user-attachments/assets/c3999dfd-b1b8-40a8-8c1c-ebe31282f590" />
<img width="1552" height="146" alt="image" src="https://github.com/user-attachments/assets/58e125ad-c757-4027-b3c2-11e5ba6ed026" />
<img width="1260" height="761" alt="image" src="https://github.com/user-attachments/assets/b064a3f4-38f6-46f8-96a9-f94285d68ba0" />
<img width="1260" height="761" alt="image" src="https://github.com/user-attachments/assets/894f408e-a206-42f2-88e8-eaa3c7bbcde2" />
<img width="1920" height="234" alt="image" src="https://github.com/user-attachments/assets/99093153-93eb-4a5d-91ef-85c4c096a7e2" />
Le patch est appliqué correctement ! La méthode retourne maintenant toujours false
<img width="1920" height="582" alt="image" src="https://github.com/user-attachments/assets/1fae02d6-6c5e-43cf-84ae-950e5769c6e9" />
<img width="1920" height="508" alt="image" src="https://github.com/user-attachments/assets/865fa589-9b04-49b1-9acd-9fc6e1801042" />
<img width="1294" height="844" alt="image" src="https://github.com/user-attachments/assets/074b799a-2493-42e2-94bd-35d3d2cacb3b" />
Parfait ! On voit exactement le flux dans onCreate :  

invoke-static {p1}, isDeviceRooted()   ← on a déjà patché ✅
move-result p1
if-eqz p1, :cond_0                     ← si false → saute à cond_0 ✅
...finish() / exit()                   ← sera ignoré ✅
:cond_0                                ← l'app continue ✅



Notre patch fonctionne correctement. La détection root est bypassée.  
Maintenant on recompile et signe l'APK

<img width="1025" height="330" alt="image" src="https://github.com/user-attachments/assets/ee11341d-558b-4b6b-afe9-6bf55a00d664" />

La recompilation a réussi ! ✅
Maintenant on signe l'APK

<img width="1521" height="453" alt="image" src="https://github.com/user-attachments/assets/9a8fcef4-40d2-4570-8fc5-61d2f14b512d" />
<img width="1521" height="576" alt="image" src="https://github.com/user-attachments/assets/ffa31dc9-3736-4d3a-ad62-96217797dfb5" />


