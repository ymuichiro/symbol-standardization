# Fully onchain png

チェーン上に画像データを保存する

## Format

```
Aggregate Complete
  ├── [header] inner transaction
  |    └── transfer transaction with mosaic id ***
  └── [body] inner transactions
       └── transfer transaction with binary
```

## header

transfer transaction を以下の形式で発行するものとする。

### mosaic

mosaic id ... xxxx

### message

#### type

plain

#### header body

```json
{
  "s-code": 1,
  "s-name": "fully-onchain-png",
  "file-type": "image/png",
  "body-hashs": ["xxxxxxxxx"]
}
```

## body

transfer transaction の message へ binary として格納する
