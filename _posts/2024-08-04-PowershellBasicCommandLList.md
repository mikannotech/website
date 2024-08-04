---
title: "PowerShell 基本コマンド"
categories:
  - プログラミング
tags:
  - Powershell
---
## 1. `Get-Command`

- 説明: 利用可能なコマンドレットを表示

```powershell
Get-Command -Name *process*

```

## 2. `Get-Help`

- 説明: コマンドレットのヘルプ情報を表示

```powershell
Get-Help Get-Process

```

## 3. `Get-Process`

- 説明: 実行中のプロセスを表示

```powershell
Get-Process | Where-Object { $_.CPU -gt 10 }

```

## 4. `Get-Service`

- 説明: システムサービスの状態を表示

```powershell
Get-Service | Where-Object { $_.Status -eq "Running" }

```

## 5. `Get-ChildItem` (別名: `dir`, `ls`)

- 説明: ディレクトリの内容をリスト表示

```powershell
Get-ChildItem -Path C:\\ -Recurse -Filter *.txt

```

## 6. `Set-Location` (別名: `cd`)

- 説明: 現在のディレクトリを変更

```powershell
Set-Location C:\\Users\\YourUsername\\Documents

```

## 7. `New-Item` (別名: `mkdir`)

- 説明: 新しいファイルやディレクトリを作成

```powershell
New-Item -Path "C:\\Temp" -ItemType Directory

```

## 8. `Copy-Item` (別名: `cp`)

- 説明: ファイルやディレクトリをコピー

```powershell
Copy-Item "C:\\source\\file.txt" -Destination "C:\\destination"

```

## 9. `Move-Item` (別名: `mv`)

- 説明: ファイルやディレクトリを移動

```powershell
Move-Item "C:\\OldFolder\\*" -Destination "C:\\NewFolder"

```

## 10. `Remove-Item` (別名: `rm`, `del`)

- 説明: ファイルやディレクトリを削除

```powershell
Remove-Item "C:\\Temp\\*.tmp" -Force

```

## 11. `Write-Output` (別名: `echo`)

- 説明: コンソールに出力を表示

```powershell
Write-Output "Hello, PowerShell!"

```

## 12. `Select-Object`

- 説明: オブジェクトのプロパティを選択して表示

```powershell
Get-Process | Select-Object Name, CPU, Memory

```

## 13. `Where-Object`

- 説明: 条件に基づいてオブジェクトをフィルタリング

```powershell
Get-Service | Where-Object { $_.Status -eq "Running" }

```

## 14. `Sort-Object`

- 説明: オブジェクトを並べ替え

```powershell
Get-ChildItem | Sort-Object Length -Descending

```

## 15. `Invoke-WebRequest`

- 説明: Webリクエストを送信し、結果を取得

```powershell
Invoke-WebRequest -Uri "<https://example.com>" | Select-Object -ExpandProperty Content

```

## 16. `Format-List`

- 説明: オブジェクトのプロパティをリスト形式で表示

```powershell
Get-Process | Format-List Name, Id, CPU

```

## 17. `Out-File`

- 説明: 出力をファイルに保存

```powershell
Get-Process | Out-File C:\\processes.txt

```

## 18. `Import-Csv` / `Export-Csv`

- 説明: CSVファイルの読み込みと書き出し

```powershell
Import-Csv C:\\data.csv | Where-Object { $_.Age -gt 30 } | Export-Csv C:\\filtered_data.csv

```

## 19. `Measure-Object`

- 説明: オブジェクトの統計情報を計算

```powershell
Get-ChildItem | Measure-Object Length -Sum -Average -Maximum -Minimum

```

## 20. `Compare-Object`

- 説明: 2つのオブジェクトセットの差異を比較

```powershell
Compare-Object (Get-Content file1.txt) (Get-Content file2.txt)


また、Get-Helpコマンドを使用するとコマンドレットの使い方を調べられる。
