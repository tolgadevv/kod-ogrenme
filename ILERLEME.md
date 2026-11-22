# İlerleme

## Durum (22 Kasım 2026)

- **Coddy:** başlangıç pratikleri ("bu kod ekrana ne basar?"). Dil: *(sorulacak)*.
- **Bitti:** Ders 1 — Yaş hesabı (`dersler/01-yas-hesabi.md`). Alıştırma: 2/2 doğru (ilk soruyu birlikte çözdük).
- **Yarım kalan:** "Ekrana ne basar?" alıştırması (aşağıda). Bir sonraki oturuma bununla başla.
- **Sıradaki dersler (öneri):**
  2. Sunucuda `docker compose` ne çalıştırıyor? (Wisp sunucusu Hetzner'e kurulurken işe yarar)
  3. CI sonucu nasıl okunur? (yeşil / kırmızı, hata mesajını bulmak)
  4. Bir ekran nasıl çizilir? (Compose'a ilk bakış)
  5. Listeler ve döngüler (`for`, `listOf`)

## Öğrenilen kavramlar

- `val` (sabit) ve `var` (değişebilir) — hafıza ipucu: **var**iable / **val**ue
- Fonksiyon: malzeme (parametre) alıp sonuç veren makine; `fun`, parametre türü (`Int`), dönüş türü (`Boolean`)
- `if` ve `return`; `else`
- Operatörler: `||` veya, `&&` ve, `==` eşit mi (tek `=` değer verir), `!` değil, `>=`, `<`, `..` aralık, `!in`
- `Boolean`: yalnızca `true` / `false`
- Tek doğruluk kaynağı: önemli değer tek yerde (`const val MIN_AGE = 18`)
- Testler: `assertTrue` / `assertFalse` kodun doğruluğunu denetler
- Yeni gördü (henüz alıştırmasız): `println`, yazı içinde `$değişken`

## Yarım kalan alıştırma

Bu kod ekrana ne basar?

```kotlin
val ad = "Tolga"
var mesaj = 3
mesaj = mesaj + 2

if (mesaj > 4) {
    println("$ad, $mesaj yeni mesajın var")
} else {
    println("Yeni mesaj yok")
}
```

A) `Tolga, 3 yeni mesajın var` · B) `Tolga, 5 yeni mesajın var` · C) `Yeni mesaj yok` · D) `$ad, $mesaj yeni mesajın var`

(Cevap: B. Önce Tolga'ya sor, cevabı verme.)
