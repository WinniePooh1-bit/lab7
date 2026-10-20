cat << 'EOF' > bugs/bug-03.md
# BUG-03: API /api/books руу дутуу JSON илгээхэд 400 бус 500 Server Error буцааж байна

* **Орчин:** Node.js v20, curl 8.0, Windows 11, 2026-10-20[cite: 4]
* **Урьдчилсан нөхцөл:** node app.js шинээр асаасан[cite: 4]

## Дахин гаргах алхам
1. Терминал нээнэ[cite: 4].
2. Дараах тушаалыг ажиллуулна:
   `curl -i -X POST http://localhost:3000/api/books -H "Content-Type: application/json" -d '{"title": "Test"}'`[cite: 4]

* **Хүлээгдэж байсан:** Шаардлагатай талбар дутуу тул HTTP Status 400 ERROR_BAD_REQUEST буцах[cite: 4].
* **Бодит үр дүн:** HTTP Status 500 Internal Server Error буцаж байна[cite: 4].

* **Ноцтой байдал:** Major (API-ийн алдаа боловсруулалт буруу)[cite: 4]
* **Хавсралт:** evidence/bug-03-curl.txt[cite: 4]
* **Олдсон аялал:** Saboteur Tour[cite: 4]
