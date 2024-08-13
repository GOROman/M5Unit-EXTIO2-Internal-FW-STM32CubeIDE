# EXTIO2 の STM32側のファームウェアを STM32CubeIDE でビルド可能にしたもの

## やったこと

1. .iocファイルだけを元のプロジェクトから STM32CubeIDE で読み込んで新規プロジェクトを作成
2. バージョンが違うのでmigrateする
3. コード生成し、ビルドを行う
4. Include 先を追加( flash, i2c_ex, servo, ws2812 )
5. 元のプロジェクトから、Core フォルダなどのファイルで上書きする
6. #include "arm_math.h" をコメントアウト
7. Debug ビルドだと FLASH 容量オーバーするので Release ビルドでビルド
   
