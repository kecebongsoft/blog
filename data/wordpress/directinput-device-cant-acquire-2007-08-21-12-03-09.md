title:DirectInput device cant acquire
date:2007-08-21 12:03:09

Setelah beberapa hari yang lalu mencoba mengulik Direct3D 9, akhirnya dakuw bisa juga membuat objek-objek primitif seperti bola, silinder, kubus, dsb. Hehehehe.. Seneng rasanya bisa bereksplorasi di dunia 3D, banyak perhitungan matematis yang dulunya dakuw nggak suka sekarang jadi cinta. Tapi selama ini untuk keyboard-event-handlernya masih pakai yang bawaan windows, alhasil setiap kali menggerakan objek menggunakan keyboard, gerakannya selalu patah-patah. Makanya tadi malam langsung ngulik DirectInput yang memang difungsikan khusus untuk keyboard event handler di DirectX. Tapi malah trouble, Device nya nggak bisa di acquire, sialan!. Padahal sudah ngikutin tutorial yang ada di SDK Documentationnya, sampe jam 12 malam blon kelar-kelar juga, tetep aja nggak bisa di acquire. Akhirnya
<a href="http://kecebongsoft.wordpress.com/2007/08/21/tek-dung/">
 tek dung
</a>
juga kira-kira satu jam, eh malah dapet mimpi, seperti wangsit yang kasih tahu bahwa untuk meng-acquire device, variable hInst dan hWnd nya mesti di init dulu atau dengan kata lain window program kita mesti nongol dulu baru bisa acquire device keyboard. Dor! Kebangun, langsung coba dan ternyata bisa ^_^. Hehehe.. thanks God.

Jadi buat temen-temen yang lagi coba-coba DirectInput di C++, pastikan dulu class windownya udah diregister, windownya udah di tampilin, baru acquire device directinputnya. Kalau instance window (hInst dan hWnd) masih null, sampe kiamat kesepuluh kagak bakal ngepek!.
