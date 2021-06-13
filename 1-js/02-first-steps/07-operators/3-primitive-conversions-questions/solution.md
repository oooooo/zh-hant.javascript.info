
```js no-beautify
"" + 1 + 0 = "10" //（1）
"" - 1 + 0 = -1 //（2）
true + false = 1
6 / "3" = 2
"2" * "3" = 6
4 + 5 + "px" = "9px"
"$" + 4 + 5 = "$45"
"4" - 2 = 2
"4px" - 2 = NaN
7 / 0 = Infinity
" -9  " + 5 = " -9  5" // (3)
" -9  " - 5 = -14 // (4)
null + 1 = 1 // (5)
undefined + 1 = NaN // (6)
" \t \n" - 2 = -2 // (7)
```

1. 字串的加法 `"" + 1` 會轉換 `1` 為字串：`"" + 1 = "1"`，然後得到 `"1" + 0` 再利用一樣的規則。
2. 減法 `-`（就像多數數學運算）只能用在數值上，它將空字串 `""` 轉成 `0`。
3. 字串的加法會將數值 `5` 視為字串接在其後。
4. 減法總是會轉換至數值，所以把 `"  -9  "` 變成數值 `-9`（忽略環繞的空白）。
5. `null` 經由數值轉換變成 `0`。
6. `undefined` 經由數值轉換變成 `NaN`。
7. 在字串被轉成數值時，頭尾的空白字元們都會被截斷。這整個字串就只包含了空白字元們，如 `\t`、`\n` 和 "常規" 的空白，所以跟空字串一樣會變成 `0`。
