**VIA REGEX**

1 - :'<,'>s/^/INSERT INTO tabela values ('/g
2 - :'<,'>s/,/', '/g
3 - :'<,'>s/$/');/g

**VIA MACRO**

1 - qa
2 - I + ' + f, + ' + esc +
3 - ESC + q
4- Find/replace
  - :'<,'>normal @a

Dados fakes - CSV https://www.mockaroo.com/

1,Clim,Farraway,cfarraway0@topsy.com,Male,86.28.50.192
2,Arin,Pearcey,apearcey1@weibo.com,Male,178.119.153.99
3,Cy,Presdee,cpresdee2@elegantthemes.com,Male,147.175.212.225
4,Laurella,Schooley,lschooley3@taobao.com,Female,110.152.166.113
5,Estrellita,Will,ewill4@cam.ac.uk,Female,56.69.80.161
6,Alla,Bram,abram5@businessweek.com,Female,100.181.82.82
7,Goober,Kippins,gkippins6@cafepress.com,Male,2.90.155.178
8,Rosalynd,Redmond,rredmond7@mapquest.com,Female,246.250.232.101
9,Fernando,Chrichton,fchrichton8@sourceforge.net,Male,210.131.198.60
10,Justin,Wadge,jwadge9@japanpost.jp,Male,109.43.189.59
11,Arley,Carlin,acarlina@globo.com,Male,116.210.75.221
12,Ara,Snow,asnowb@cnn.com,Female,49.227.7.53
13,Paulette,Biasini,pbiasinic@free.fr,Female,79.189.158.25
14,Janna,Lineham,jlinehamd@irs.gov,Female,215.136.168.18
15,Deanna,Longman,dlongmane@vkontakte.ru,Female,194.194.252.34
