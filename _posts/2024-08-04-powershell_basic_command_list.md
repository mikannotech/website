---
title: "PowerShell 基本コマンド"
categories:
  - プログラミング
tags:
  - Powershell
---

## `Get-Command`
利用可能なコマンドレットを表示
```powershell
Get-Command -Name *process*
```

## `Get-Help`
コマンドレットのヘルプ情報を表示
```powershell
Get-Help Get-Process
```

## `Get-Process`
実行中のプロセスを表示
```powershell
Get-Process | Where-Object { $_.CPU -gt 10 }
```

## `Get-Service`
システムサービスの状態を表示
```powershell
Get-Service | Where-Object { $_.Status -eq "Running" }
```

## `Get-ChildItem` (別名: `dir`, `ls`)
ディレクトリの内容をリスト表示
```powershell
Get-ChildItem -Path C:\\ -Recurse -Filter *.txt
```

## `Set-Location` (別名: `cd`)
現在のディレクトリを変更
```powershell
Set-Location C:\\Users\\YourUsername\\Documents
```

## `New-Item` (別名: `mkdir`)
新しいファイルやディレクトリを作成
```powershell
New-Item -Path "C:\\Temp" -ItemType Directory
```

## `Copy-Item` (別名: `cp`)
ファイルやディレクトリをコピー
```powershell
Copy-Item "C:\\source\\file.txt" -Destination "C:\\destination"
```

## `Move-Item` (別名: `mv`)
ファイルやディレクトリを移動
```powershell
Move-Item "C:\\OldFolder\\*" -Destination "C:\\NewFolder"
```

## `Remove-Item` (別名: `rm`, `del`)
ファイルやディレクトリを削除
```powershell
Remove-Item "C:\\Temp\\*.tmp" -Force
```

## `Write-Output` (別名: `echo`)
コンソールに出力を表示
```powershell
Write-Output "Hello, PowerShell!"
```

## `Select-Object`
オブジェクトのプロパティを選択して表示
```powershell
Get-Process | Select-Object Name, CPU, Memory
```

## `Where-Object`
条件に基づいてオブジェクトをフィルタリング
```powershell
Get-Service | Where-Object { $_.Status -eq "Running" }
```

## `Sort-Object`
オブジェクトを並べ替え
```powershell
Get-ChildItem | Sort-Object Length -Descending
```

## `Invoke-WebRequest`
Webリクエストを送信し、結果を取得
```powershell
Invoke-WebRequest -Uri "https://example.com" | Select-Object -ExpandProperty Content
```

## `Format-List`
オブジェクトのプロパティをリスト形式で表示
```powershell
Get-Process | Format-List Name, Id, CPU
```

## `Out-File`
出力をファイルに保存
```powershell
Get-Process | Out-File C:\\processes.txt
```

## `Import-Csv` / `Export-Csv`
CSVファイルの読み込みと書き出し
```powershell
Import-Csv C:\\data.csv | Where-Object { $_.Age -gt 30 } | Export-Csv C:\\filtered_data.csv
```

## `Measure-Object`
オブジェクトの統計情報を計算
```powershell
Get-ChildItem | Measure-Object Length -Sum -Average -Maximum -Minimum
```

## `Compare-Object`
2つのオブジェクトセットの差異を比較
```powershell
Compare-Object (Get-Content file1.txt) (Get-Content file2.txt)
```

また、Get-Help -online でコマンドレットの公式ドキュメントに飛べる。

