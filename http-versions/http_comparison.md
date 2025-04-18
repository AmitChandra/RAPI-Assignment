
# 📊 HTTP/1.1 vs HTTP/2 vs HTTP/3

| Feature                        | **HTTP/1.1**                          | **HTTP/2**                             | **HTTP/3**                          |
|:--------------------------------|:--------------------------------------|:----------------------------------------|:------------------------------------|
| **Connection Type**            | TCP                                    | TCP                                      | QUIC (built on UDP)                  |
| **Multiplexing**               | ❌ No — one request at a time per connection | ✅ Yes — multiple streams over one connection | ✅ Yes — multiple streams, no blocking |
| **Head-of-Line Blocking**       | ❌ Yes                                 | ⚠️ Partially (TCP-level)                | ✅ No                                |
| **Header Compression**          | ❌ No (plain text)                     | ✅ Yes (HPACK)                           | ✅ Yes (QPACK)                       |
| **Server Push**                 | ❌ No                                   | ✅ Yes                                    | ✅ Yes                                |
| **Encryption (TLS/SSL)**        | Optional                               | Optional                                 | ✅ Always encrypted (TLS 1.3 over QUIC) |
| **Request Prioritization**      | ❌ No                                   | ✅ Yes                                    | ✅ Yes                                |
| **Latency**                     | High                                   | Lower                                    | Very low                             |
| **Connection Establishment Speed** | Slow (TCP + optional TLS handshake)    | Faster (TCP + TLS)                       | Fastest (0-RTT with QUIC)            |
| **Adoption**                    | Mature, widely supported               | Increasing rapidly                       | Emerging, modern browsers & services |

---

## 📌 Summary

- **HTTP/1.1**: Reliable, but suffers from head-of-line blocking, high latency, and connection inefficiencies.
- **HTTP/2**: Huge improvement — introduces multiplexing, header compression, and server push.
- **HTTP/3**: Modern, faster, built on **QUIC (UDP)** — eliminates head-of-line blocking, accelerates secure connections, and is future-ready.
