# Ders 1 — Yaş hesabı (22 Kasım 2026)

Wisp'in 18+ kuralı için yazılan kodun sadeleştirilmiş hali (Wisp'te `core/Age.kt`):

```kotlin
const val MIN_AGE = 18

fun isAdult(
    birthYear: Int, birthMonth: Int, birthDay: Int,
    todayYear: Int, todayMonth: Int, todayDay: Int,
): Boolean {
    if (birthMonth !in 1..12) return false
    if (birthYear < 1900) return false

    var age = todayYear - birthYear
    if (todayMonth < birthMonth || (todayMonth == birthMonth && todayDay < birthDay)) age--

    return age >= MIN_AGE
}
```

## Satır satır

1. `const val MIN_AGE = 18`: değişmeyen değer. Yaş sınırı değişirse yalnızca bu satır değişir (tek doğruluk kaynağı).
2. `fun isAdult(...): Boolean`: fonksiyon = makine. Parantez içi malzemeler (`birthYear: Int` = tam sayı), `Boolean` = sonuç
   yalnızca `true`/`false`.
3. `if (birthMonth !in 1..12) return false`: ay 1-12 arasında değilse hemen "hayır" de (`!` = değil).
4. `var age = todayYear - birthYear`: `var`, çünkü bir sonraki satırda değişebilir.
5. Doğum günü bu yıl gelmediyse `age--` (yaştan 1 çıkar). `||` veya, `&&` ve, `==` eşit mi.
6. `return age >= MIN_AGE`: 18 ve üstüyse "evet".

## Birlikte çözülen örnek

`isAdult(2000, 5, 10, 2026, 3, 1)` → 10 Mayıs 2000 doğumlu, bugün 1 Mart 2026.
Ay geçerli ✓ · yıl ≥ 1900 ✓ · `age` = 26 · Mart < Mayıs → doğum günü gelmedi → `age` = 25 · 25 ≥ 18 → **true**.

## Alıştırma

- Yaş sınırını 16 yapmak: yalnızca `const val MIN_AGE = 16` → Tolga: **B ✓**
- `val renk` / `var sayi`: hangisi değişir? → `sayi` (`var`) → Tolga: **B ✓**
