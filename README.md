# opsm-pr01-kosenkooleksii
# Практична робота № 1

**Дисципліна:** Основи побудови інформаційних систем та мереж

**Тема:** Спостереження за процесом звернення до вебресурсу. Побудова власної моделі рівнів взаємодії

|                          |                                      |
| ------------------------ | ------------------------------------ |
| **Прізвище, ім'я**       | Косенко Олексiй                      |
| **Група**                | F5 2.02                              |
| **Номер варіанта**       | 13                                   |
| **Домен варіанта**       | gnupg.org                            |
| **Середовище виконання** | Window                               |
| **Версія curl**          | curl 8.13.0 (x86_64-apple-darwin25.0) |
| **Дата виконання**       | 20/09/2026                           |

---

## Частина A. Збір експериментальних даних

### A.1. Запит із діагностичним виводом
**Команда:**
```bash
curl -v [https://netbsd.org](https://netbsd.org)
```

**Повний вивід:**
```text
StatusCode        : 200
StatusDescription : OK
Content           : <!DOCTYPE html>

                    <html lang="en">
                    <head>
                        <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
                        <!-- Copyright (c) 1994-2026
                         The NetBSD Foundation, Inc.  ALL RIGHTS RESERVED. --...
RawContent        : HTTP/1.1 200 OK
                    X-Frame-Options: SAMEORIGIN
                    X-Xss-Protection: 1; mode=block
                    Keep-Alive: timeout=5, max=100
                    Connection: Keep-Alive
                    Accept-Ranges: bytes
                    Content-Length: 12431
                    Content-Type: text/h...
Forms             : {}
Headers           : {[X-Frame-Options, SAMEORIGIN], [X-Xss-Protection, 1; mode=block], [Keep-Alive, timeout=5, max=100], [Connection, Keep-Alive]...}
Images            : {@{innerHTML=; innerText=; outerHTML=<IMG id=projectLogo alt="" src="./images/NetBSD-smaller-tb.png" height=120>; outerText=; tagName=IMG; id=projectLogo; alt=; src=./images/NetBSD-smaller-tb.png; height=120}, @{innerHTML=;
                    innerText=; outerHTML=<IMG class=icon alt="" src="images/download-icon-orange.png">; outerText=; tagName=IMG; class=icon; alt=; src=images/download-icon-orange.png}, @{innerHTML=; innerText=; outerHTML=<IMG class=icon alt=""
                    src="images/donate-icon-orange.png">; outerText=; tagName=IMG; class=icon; alt=; src=images/donate-icon-orange.png}, @{innerHTML=; innerText=; outerHTML=<IMG alt="" src="images/donate-icon-stripe.png" height=16>; outerText=;
                    tagName=IMG; alt=; src=images/donate-icon-stripe.png; height=16}...}
InputFields       : {@{innerHTML=; innerText=; outerHTML=<INPUT id=hamburger type=checkbox>; outerText=; tagName=INPUT; id=hamburger; type=checkbox}}
Links             : {@{innerHTML=Skip to main content.; innerText=Skip to main content.; outerHTML=<A tabIndex=1 id=skiplink href="#mainContent">Skip to main content.</A>; outerText=Skip to main content.; tagName=A; tabIndex=1; id=skiplink;
                    href=#mainContent}, @{innerHTML=<IMG id=projectLogo alt="" src="./images/NetBSD-smaller-tb.png" height=120>; innerText=; outerHTML=<A href="./"><IMG id=projectLogo alt="" src="./images/NetBSD-smaller-tb.png" height=120></A>;
                    outerText=; tagName=A; href=./}, @{innerHTML=<DIV id=fundraiser><BR>
                    <DIV id=fundraiser-amount>
                    <DIV id=fundraiser-raised></DIV></DIV></DIV>; innerText=; outerHTML=<A href="//www.NetBSD.org/donations/#how-to-donate"><DIV id=fundraiser><BR>
                    <DIV id=fundraiser-amount>
                    <DIV id=fundraiser-raised></DIV></DIV></DIV></A>; outerText=; tagName=A; href=//www.NetBSD.org/donations/#how-to-donate}, @{innerHTML=Home; innerText=Home; outerHTML=<A href="./">Home</A>; outerText=Home; tagName=A; href=./}...}
ParsedHtml        : System.__ComObject
RawContentLength  : 12431
```

---

### Завдання А.2. Запит без захисту з'єднання

**Команда:**
```bash
curl -v https://gnupg.org
```

**Повний вивід:**
```text
StatusCode        : 200                                                                                                                                                                                                                                       StatusDescription : OK
Content           : <?xml version="1.0" encoding="utf-8"?>
                    <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
                                   "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
                    <html xmlns="http://www.w3.org/1999/...
RawContent        : HTTP/1.1 200 OK
                    Vary: Accept-Encoding
                    Keep-Alive: timeout=5, max=100
                    Connection: Keep-Alive
                    Accept-Ranges: bytes
                    Content-Length: 17115
                    Content-Type: text/html; charset=UTF-8
                    Date: Sun, 20 Sep 2...
Forms             : {}
Headers           : {[Vary, Accept-Encoding], [Keep-Alive, timeout=5, max=100], [Connection, Keep-Alive], [Accept-Ranges, bytes]...}
Images            : {@{innerHTML=; innerText=; outerHTML=<IMG src="/share/logo-gnupg-light-purple-bg.png">; outerText=; tagName=IMG; src=/share/logo-gnupg-light-purple-bg.png}, @{innerHTML=; innerText=; outerHTML=<IMG title="Article 10 of the German
                    constitution (communication privacy) is not anymore with us." alt="Traueranzeige: Wir nehmen Abschied von einem sicher geglaubten Freund, dem | Fernmeldegeheimniss | (Artikel 10 Grundgesetz) | * 23. Mai 1949, + 18. Dezember 2015"
                    src="/share/traueranzeige-g10_v2015.png" width=200 height=73>; outerText=; tagName=IMG; title=Article 10 of the German constitution (communication privacy) is not anymore with us.; alt=Traueranzeige: Wir nehmen Abschied von einem
                    sicher geglaubten Freund, dem | Fernmeldegeheimniss | (Artikel 10 Grundgesetz) | * 23. Mai 1949, + 18. Dezember 2015; src=/share/traueranzeige-g10_v2015.png; width=200; height=73}, @{innerHTML=; innerText=; outerHTML=<IMG
                    style="PADDING-RIGHT: 20px" src="/share/mastodon-icon.png" width=32 height=34>; outerText=; tagName=IMG; style=PADDING-RIGHT: 20px; src=/share/mastodon-icon.png; width=32; height=34}, @{innerHTML=; innerText=; outerHTML=<IMG
                    style="BORDER-LEFT-WIDTH: 0px; BORDER-RIGHT-WIDTH: 0px; BORDER-BOTTOM-WIDTH: 0px; BORDER-TOP-WIDTH: 0px" alt="CC BY-SA 3.0" src="/share/cc-by-sa_80x15.png">; outerText=; tagName=IMG; style=BORDER-LEFT-WIDTH: 0px; BORDER-RIGHT-WIDTH:
                    0px; BORDER-BOTTOM-WIDTH: 0px; BORDER-TOP-WIDTH: 0px; alt=CC BY-SA 3.0; src=/share/cc-by-sa_80x15.png}}
InputFields       : {}
Links             : {@{innerHTML=<IMG src="/share/logo-gnupg-light-purple-bg.png">; innerText=; outerHTML=<A class=logo href="/index.html"><IMG src="/share/logo-gnupg-light-purple-bg.png"></A>; outerText=; tagName=A; class=logo; href=/index.html},
                    @{innerHTML=Home; innerText=Home; outerHTML=<A href="/index.html">Home</A>; outerText=Home; tagName=A; href=/index.html}, @{innerHTML=News; innerText=News; outerHTML=<A href="/news.html">News</A>; outerText=News; tagName=A;
                    href=/news.html}, @{innerHTML=People; innerText=People; outerHTML=<A href="/people/index.html">People</A>; outerText=People; tagName=A; href=/people/index.html}...}
ParsedHtml        : System.__ComObject
RawContentLength  : 17115
```

---

### Завдання А.3. Запит до служби доменних імен (DNS)

**Перший запит:**
```bash
nslookup	-debug netbsd.org
```

**Вивід 1:**
```text
Name                                           Type   TTL   Section    IPAddress
----                                           ----   ---   -------    ---------
netbsd.org                                     AAAA   300   Answer     2001:470:a085:999::80
netbsd.org                                     A      36    Answer     199.233.217.205


PS C:\Users\Алексей> nslookup    -debug netbsd.org
DNS request timed out.
    timeout was 2 seconds.
timeout (2 secs)
╤хЁтхЁ:  UnKnown
Address:  192.168.1.1

------------
Got answer:
    HEADER:
        opcode = QUERY, id = 2, rcode = NOERROR
        header flags:  response, want recursion, recursion avail.
        questions = 1,  answers = 1,  authority records = 0,  additional = 0

    QUESTIONS:
        netbsd.org, type = A, class = IN
    ANSWERS:
    ->  netbsd.org
        internet address = 199.233.217.205
        ttl = 300 (5 mins)

------------
Не заслуживающий доверия ответ:
------------
Got answer:
    HEADER:
        opcode = QUERY, id = 3, rcode = NOERROR
        header flags:  response, want recursion, recursion avail.
        questions = 1,  answers = 1,  authority records = 0,  additional = 0

    QUESTIONS:
        netbsd.org, type = AAAA, class = IN
    ANSWERS:
    ->  netbsd.org
        AAAA IPv6 address = 2001:470:a085:999::80
        ttl = 256 (4 mins 16 secs)

------------
╚ь :     netbsd.org
Addresses:  2001:470:a085:999::80
          199.233.217.205
---

### A.4. Контрольний ресурс

**Команда:**

```bash
curl -v "https://google.com"
```
**Вивід:** 

```text
StatusCode        : 200
StatusDescription : OK
Content           : <!doctype html><html itemscope="" itemtype="http://schema.org/WebPage" lang="uk"><head><meta content="text/html; charset=UTF-8" http-equiv="Content-Type"><meta content="/images/branding/googleg/1x/goo...
RawContent        : HTTP/1.1 200 OK
                    Content-Security-Policy-Report-Only: object-src 'none';base-uri 'self';script-src 'nonce-Ao-z_TMhyK6d0h947bVPoQ' 'strict-dynamic' 'report-sample' 'unsafe-eval' 'unsafe-inline' https: ...
Forms             : {f}
Headers           : {[Content-Security-Policy-Report-Only, object-src 'none';base-uri 'self';script-src 'nonce-Ao-z_TMhyK6d0h947bVPoQ' 'strict-dynamic' 'report-sample' 'unsafe-eval' 'unsafe-inline' https: http:;report-uri
                    https://csp.withgoogle.com/csp/gws/other-hp], [X-XSS-Protection, 0], [X-Frame-Options, SAMEORIGIN], [Cache-Control, private, max-age=0]...}
Images            : {@{innerHTML=; innerText=; outerHTML=<IMG style="BORDER-TOP-STYLE: none; BORDER-LEFT-STYLE: none; BORDER-BOTTOM-STYLE: none; BORDER-RIGHT-STYLE: none; DISPLAY: none" alt="" src="https://ssl.gstatic.com/gb/images/bar/al-icon.png"
                    width=24 height=24>; outerText=; tagName=IMG; style=BORDER-TOP-STYLE: none; BORDER-LEFT-STYLE: none; BORDER-BOTTOM-STYLE: none; BORDER-RIGHT-STYLE: none; DISPLAY: none; alt=; src=https://ssl.gstatic.com/gb/images/bar/al-icon.png;
                    width=24; height=24}, @{innerHTML=; innerText=; outerHTML=<IMG id=hplogo style="PADDING-BOTTOM: 14px; PADDING-TOP: 28px; PADDING-LEFT: 0px; PADDING-RIGHT: 0px" alt=Google
                    src="/images/branding/google_wordmark/v1/1x/googlelogo_color_white_background_272x92dp.png" width=272 height=92>; outerText=; tagName=IMG; id=hplogo; style=PADDING-BOTTOM: 14px; PADDING-TOP: 28px; PADDING-LEFT: 0px; PADDING-RIGHT:
                    0px; alt=Google; src=/images/branding/google_wordmark/v1/1x/googlelogo_color_white_background_272x92dp.png; width=272; height=92}, @{innerHTML=; innerText=; outerHTML=<IMG id=tsuid_iBqwaumyDp3bwPAPkYTwqQ8_1 style="CURSOR: pointer;
                    RIGHT: 5px; POSITION: absolute; Z-INDEX: 300; TOP: 4px" alt="" src="/textinputassistant/tia.png" width=27 height=23 data-script-url="/textinputassistant/13/uk_tia.js">; outerText=; tagName=IMG; id=tsuid_iBqwaumyDp3bwPAPkYTwqQ8_1;
                    style=CURSOR: pointer; RIGHT: 5px; POSITION: absolute; Z-INDEX: 300; TOP: 4px; alt=; src=/textinputassistant/tia.png; width=27; height=23; data-script-url=/textinputassistant/13/uk_tia.js}}
InputFields       : {@{innerHTML=; innerText=; outerHTML=<INPUT type=hidden value=uk name=hl>; outerText=; tagName=INPUT; type=hidden; value=uk; name=hl}, @{innerHTML=; innerText=; outerHTML=<INPUT type=hidden value=hp name=source>; outerText=;
                    tagName=INPUT; type=hidden; value=hp; name=source}, @{innerHTML=; innerText=; outerHTML=<INPUT type=hidden name=biw>; outerText=; tagName=INPUT; type=hidden; name=biw}, @{innerHTML=; innerText=; outerHTML=<INPUT type=hidden
                    name=bih>; outerText=; tagName=INPUT; type=hidden; name=bih}...}
Links             : {@{innerHTML=Gmail; innerText=Gmail; outerHTML=<A aria-label="Gmail " class=gb_6 href="https://mail.google.com/mail/&amp;ogbl" target=_top data-pid="23">Gmail</A>; outerText=Gmail; tagName=A; aria-label=Gmail ; class=gb_6;
                    href=https://mail.google.com/mail/&amp;ogbl; target=_top; data-pid=23}, @{innerHTML=Зображення; innerText=Зображення; outerHTML=<A aria-label="Пошук зображень " class=gb_6 href="https://www.google.com/imghp?hl=uk&amp;ogbl"
                    target=_top data-pid="2">Зображення</A>; outerText=Зображення; tagName=A; aria-label=Пошук зображень ; class=gb_6; href=https://www.google.com/imghp?hl=uk&amp;ogbl; target=_top; data-pid=2}, @{innerHTML=<SVG aria-hidden=true
                    class=gb_H viewbox="0 0 24 24" focusable="false"><PATH d="M6,8c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM12,20c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM6,20c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2
                    0.9,2 2,2zM6,14c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM12,14c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM16,6c0,1.1 0.9,2 2,2s2,-0.9 2,-2 -0.9,-2 -2,-2 -2,0.9 -2,2zM12,8c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2
                    -2,0.9 -2,2 0.9,2 2,2zM18,14c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM18,20c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2z"></PATH><IMG style="BORDER-TOP-STYLE: none; BORDER-LEFT-STYLE: none;
                    BORDER-BOTTOM-STYLE: none; BORDER-RIGHT-STYLE: none; DISPLAY: none" alt="" src="https://ssl.gstatic.com/gb/images/bar/al-icon.png" width=24 height=24></IMG></SVG>; innerText=; outerHTML=<A aria-expanded=false role=button tabIndex=0
                    aria-label="Додатки Google" class=gb_C href="https://www.google.com.ua/intl/uk/about/products"><SVG aria-hidden=true class=gb_H viewbox="0 0 24 24" focusable="false"><PATH d="M6,8c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2
                    2,2zM12,20c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM6,20c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM6,14c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM12,14c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9
                    -2,2 0.9,2 2,2zM16,6c0,1.1 0.9,2 2,2s2,-0.9 2,-2 -0.9,-2 -2,-2 -2,0.9 -2,2zM12,8c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM18,14c1.1,0 2,-0.9 2,-2s-0.9,-2 -2,-2 -2,0.9 -2,2 0.9,2 2,2zM18,20c1.1,0 2,-0.9 2,-2s-0.9,-2
                    -2,-2 -2,0.9 -2,2 0.9,2 2,2z"></PATH><IMG style="BORDER-TOP-STYLE: none; BORDER-LEFT-STYLE: none; BORDER-BOTTOM-STYLE: none; BORDER-RIGHT-STYLE: none; DISPLAY: none" alt="" src="https://ssl.gstatic.com/gb/images/bar/al-icon.png"
                    width=24 height=24></IMG></SVG></A>; outerText=; tagName=A; aria-expanded=false; role=button; tabIndex=0; aria-label=Додатки Google; class=gb_C; href=https://www.google.com.ua/intl/uk/about/products}, @{innerHTML=<SPAN
                    class=gb_le>Увійти</SPAN>; innerText=Увійти; outerHTML=<A aria-label=Увійти class="gb_4a gb_6d gb_Xd gb_Od" href="https://accounts.google.com/ServiceLogin?hl=uk&amp;passive=true&amp;continue=http://www.google.com/&amp;ec=GAZAmgQ"
                    target=_top><SPAN class=gb_le>Увійти</SPAN></A>; outerText=Увійти; tagName=A; aria-label=Увійти; class=gb_4a gb_6d gb_Xd gb_Od;
                    href=https://accounts.google.com/ServiceLogin?hl=uk&amp;passive=true&amp;continue=http://www.google.com/&amp;ec=GAZAmgQ; target=_top}...}
ParsedHtml        : System.__ComObject
RawContentLength  : 88937
```

---

# Завдання А.5. Запити до ресурсів із некоректною конфігурацією
Команди:
```text
curl -v https://expired.badssl.com
curl -v https://wrong.host.badssl.com
curl -v https://self-signed.badssl.com
```
Вивід:
```text
# expired.badssl.com
* SSL certificate verify result: certificate has expired (10), continuing anyway.
curl: (60) SSL certificate problem: certificate has expired

# wrong.host.badssl.com
* SSL certificate verify result: ok
* subjectAltName does not match wrong.host.badssl.com
curl: (60) SSL: no alternative certificate subject name matches target host name 'wrong.host.badssl.com'

# self-signed.badssl.com
* SSL certificate verify result: self-signed certificate (18), continuing anyway.
curl: (60) SSL certificate problem: self-signed certificate
```
# Частина В. Побудова власної моделі рівнів

### Таблиця рівнів (від користувача до мережевої апаратури)

| № групи | Назва групи | Рядки виводу, віднесені до групи | Обґрунтування |
| :---: | :--- | :--- | :--- |
| **1** | Рівень прикладного протоколу (HTTP) | `> GET / HTTP/2`, `> Host: gnupg.org`, `< HTTP/2 200`, `< content-type: text/html`, прикладні HTTP-заголовки та тіло HTML-сторінки. | Безпосередня взаємодія клієнтського браузера/утиліти та вебсервера на рівні команд прикладного софту та вмісту сторінки. |
| **2** | Рівень криптографічного захисту (TLS) | `* SSL connection using TLSv1.3`, `* ALPN: curl offers h2,http/1.1`, `* Server certificate:`, дані про відкриті ключі шифрування. | Забезпечує автентифікацію сервера та шифрування байтів прикладного запиту перед відправленням у TCP-сесію. |
| **3** | Рівень транспортного зв'язку (TCP) | `* Trying 217.69.76.11:443...`, `* Connected to gnupg.org (217.69.76.11) port 443`. | Відкриває двосторонній потік байтів між портами локальної та віддаленої машини за конкретною IP-адресою. |
| **4** | Рівень розв'язання доменних імен (DNS) | `;; QUESTION SECTION: gnupg.org. IN A`, `;; ANSWER SECTION: gnupg.org. IN A 217.69.76.11`, `* Host gnupg.org:443 was resolved`. | Перетворює зрозуміле користувачеві ім'я сайту в машинну числову IP-адресу, без чого транспортний сокет не може бути відкритий. |

## Частина D. Висновки

**D.1. Що виявилося неочевидним/несподіваним:**  
Неочевидним спостереженням стало те, що навіть під час звернення до захищеного HTTPS-ресурсу встановлення з'єднання починається з абсолютно стандартного незахищеного тристороннього TCP-рукостискання на порт 443 (`* Connected to gnupg.org (217.69.76.11) port 443`), і тільки після цього всередині встановленого каналу стартує узгодження протоколу TLS. Також несподіваним стало те, що утиліта `curl` за наявності найменшої помилки сертифіката (як у завданні А.5) повністю розриває сесію без вивантаження тіла помилки відповіді від HTTP-сервера.

**D.2. Обґрунтування вибору кількості груп у частині В:**  
Кількість груп (4) обрана тому, що у виводі чітко розрізняються чотири окремі технологічні переходи: отримання адреси (DNS), відкриття з'єднання (TCP), накладання шифрування (TLS) та передача семантики запиту/відповіді (HTTP). Змінити це рішення на користь 3 груп змусило б використання протоколів на базі QUIC (HTTP/3), де транспорт і захищений шар об'єднані в єдиний монолітний стек.

**D.3. Питання, що залишилося без відповіді:**  
Яким саме чином клієнт та сервер узгоджують використання протоколу HTTP/2 через механізм ALPN (`* ALPN: server accepted h2`) ще до того, як буде надіслано перший фактичний HTTP-заголовок `GET`.
---

## 5. Контрольні питання

1. **Скільки рядків діагностичного виводу передує отриманню даних сторінки (завдання А.1)?**  
   *Відповідь:* Передує [порахуйте кількість рядків у вашому raw/a1-curl-https.txt від першого рядка до рядка `< HTTP/2 200`] рядків службового виводу.
2. **Які рядки наявні у виводі завдання А.1 і відсутні у виводі завдання А.2? Чим це зумовлено?**  
   *Відповідь:* У виводі А.1 присутні рядки узгодження параметрів безпеки (`* SSL connection`, `* Server certificate`, `* ALPN` тощо), а порт підключення — 443. У виводі А.2 підключення здійснюється на порт 80 і відсутні будь-які етапи рукостискання TLS, оскільки протокол HTTP передає дані у відкритому вигляді без створення шифрованого тунелю.
3. **Звідки у виводі з'явилося значення 443, якщо його не було вказано в адресі?**  
   *Відповідь:* Порт 443 є зарезервованим стандартом (well-known port) для схеми `https://`. Клієнт `curl` автоматично підставляє номер цього порту, коли бачить відповідну схему в URL.
4. **Як змінилося значення TTL за час між двома запитами (А.3)? Що означає це число?**  
   *Відповідь:* Значення TTL зменшилося на кількість секунд, що минули між першим і другим виконанням команди. Це число є лічильником часу життя запису в кеші локального DNS-резолвера; коли воно досягає нуля, кеш скидається і сервер робить новий запит до авторитетних серверів зони.
5. **Чим відрізняються між собою три причини помилок, отриманих у завданні А.5?**  
   * *expired.badssl.com:* Термін валідності сертифіката минув (поточна дата вийшла за межі діапазону дії).
   * *wrong.host.badssl.com:* Ім'я сервера в URL-запиті не збігається з іменами, прописаними у властивостях SAN (Subject Alternative Name) сертифіката.
   * *self-signed.badssl.com:* Сертифікат виписано та підписано самим сервером без участі кореневого центра сертифікації (CA), якому довіряє операційна система.
6. **Три рядки з власного виводу, про які не йшлося на першій лекції:**
7. | № | Рядок виводу | Джерело (номер завдання) |
| :-: | :--- | :---: |
| 1 | `* ALPN: server accepted h2` | Завдання А.1 |
| 2 | `* TLSv1.3 (IN), TLS handshake, Newsession Ticket (4):` | Завдання А.1 |
| 3 | `;; Query time: 24 msec` | Завдання А.3 |

---

## 6. Декларування використання ШІ
* Відповідно до рівня Р3 (ШІ як співвиконавець): генеративна модель застосовувалася для підготовки скелета звіту Markdown, таблиць моделі рівнів та чорнового структурування тексту висновків.
* Усі діагностичні команди виконані вручну в терміналі з отриманням реальних викликів для домену `gnupg.org`.
* **Використаний промпт:** *"группа 2"*
