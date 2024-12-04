# recpt1

[recpt1(STZ版)][link_recpt1]に対して以下の変更をしたものです。

* `driver/pt1_ioctl.h` からpx4_drvに付属の`ptx_ioctl.h`に変更
* チャンネル変更時に`ioctl(PTX_SET_SYSTEM_MODE)`を実行

目的は、PX-M1URとpx4_drvでチャンネルC13-C24を使えるようにしたいということです。

-----

[recpt1(STZ版)][link_recpt1]のREADMEを以下に示します。

```txt
【recpt1 HTTPサーバ版RC4 + α（STZ版）】
Linux用PT1/PT2/PT3録画プログラムです。
こちらは亜流版ですのでご注意下さい。

本家はこちら→ http://hg.honeyplanet.jp/pt1/
※ドライバー部分は本家やその他分家（↓）のものをお使い下さい。
　PT1/PT2：http://sourceforge.jp/projects/pt1dvr/
　PT3：https://github.com/m-tsudo/pt3
※libarib25はこちら→ https://github.com/stz2012/libarib25

cd recpt1/recpt1
./autogen.sh
./configure --enable-b25
make
でビルドした後、
./recpt1 録画するチャンネル 録画秒数 出力先ファイル名
で録画されます。
詳しいオプションはrecpt1 --helpをご覧下さい。

Special Thanks:
・2chの「Linuxでテレビ総合」スレッドの皆様

動作確認環境:
  Debian 11 x86_64 GNU/Linux
  Linux 5.10.0 SMP
  Ubuntu 22.04 LTS x86_64 GNU/Linux
  Linux 5.15.0 SMP
```

[link_recpt1]: https://github.com/stz2012/recpt1
