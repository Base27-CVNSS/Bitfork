# Bitfork Atlas · Phả hệ Bitcoin

**Bitfork Atlas** là bản đồ tương tác bằng tiếng Việt về hệ sinh thái Bitcoin, lấy cảm hứng từ infographic [A Map of Bitcoin Forks — Bitcoin Magazine (2019)](https://bitcoinmagazine.com/technical/infographic-map-bitcoin-forks) và mở rộng tới Litecoin, Dogecoin, Zcash, Bitcoin Private, eCash.

## Chạy và triển khai

- Mở trực tiếp file **index.html** bằng trình duyệt. Không cần cài đặt, backend hay khóa API.
- Để công bố qua GitHub Pages: vào **Settings → Pages → Build and deployment → Deploy from a branch → main / (root) → Save**.
- Khi Pages đã bật và build thành công, đường dẫn dự kiến: https://base27-cvnss.github.io/Bitfork/

## Chức năng

- Bản đồ SVG theo phong cách tuyến phân nhánh, cuộn, phóng to/thu nhỏ, điều hướng theo năm.
- Tìm kiếm nhanh và lọc **fork blockchain**, **fork mã nguồn**, **client** và **fork-merge**.
- Nhấn vào một nhánh để xem nguồn gốc, trạng thái UTXO, khác biệt kỹ thuật và các nhánh con.
- Xuất biểu đồ độc lập thành **SVG**, **PNG**; tải dữ liệu đầy đủ thành **JSON**.
- Giao diện tiếng Việt, responsive, không truy cập seed phrase hoặc ví người dùng.

## Các kiểu quan hệ khác nhau

| Phân loại | Ví dụ | Lưu ý |
| --- | --- | --- |
| Fork blockchain | Bitcoin Cash, Bitcoin Gold, Bitcoin SV, eCash | Lịch sử/trạng thái chung trước mốc chain split, sau đó theo quy tắc riêng |
| Fork mã nguồn, blockchain mới | Litecoin, Zcash, Ravencoin | **Không kế thừa UTXO hoặc số dư BTC** |
| Client/phần mềm | Bitcoin Knots, Libbitcoin, BIP148 Client, BTC1 | Không đồng nghĩa phát hành coin mới |
| Fork-merge / snapshot | Bitcoin Private | Kết hợp snapshot BTC và Zclassic, khác chain split trực tiếp |

**Bitcoin Core** là phần mềm Bitcoin. Một đồng coin khác trong nhánh Bitcoin Clashic/Bitcoin Core Sq từng mang tên tương tự nhưng **không phải Bitcoin BTC**.

**Các khoảng cách theo trục dọc được bố trí theo đồ họa, không theo tỷ lệ thời gian tuyến tính.** Không dùng tọa độ trên biểu đồ để ước tính thời gian hoặc block height chính xác.

**Bảo mật:** không nhập seed phrase, private key, WIF vào website không đáng tin cậy để tìm hoặc nhận coin fork. Trang này chỉ là sơ đồ đọc hiểu, hoàn toàn không cần kết nối ví.

## Nguồn đối chiếu

- [Bitcoin Magazine — A Map of Bitcoin Forks](https://bitcoinmagazine.com/technical/infographic-map-bitcoin-forks): nền tảng phân loại fork chain/codebase/clients.
- [Bitcoin Cash Protocol Documentation](https://documentation.cash/project-history.html): lịch sử nâng cấp BCH.
- [Zcash — mã nguồn GitHub](https://github.com/zcash/zcash): nhánh công nghệ Zcash.
- [Bitcoin Private — mã nguồn](https://github.com/BTCPrivate/BitcoinPrivate): mô hình snapshot BTC + ZCL.
- [List of Bitcoin Forks](https://en.wikipedia.org/wiki/List_of_bitcoin_forks): đối chiếu các mốc fork (nguồn tổng hợp).

## Mở rộng

Toàn bộ mã nằm trong **index.html**. Hai mảng dữ liệu **N** (các nút) và **EVENTS** (sự kiện) có thể được bổ sung theo thời gian. Mỗi nút bao gồm mã nhận dạng, tên, ticker, năm, vị trí sơ đồ, loại quan hệ, nút cha, diễn giải và nguồn.

Sơ đồ hiện tại là một **bộ dữ liệu chọn lọc**, không phải mọi blockchain từng được tạo ra từ Bitcoin. Tình trạng hoạt động, khả năng giao dịch và khả năng nhận coin fork lịch sử không được bảo đảm.

Trang là bản diễn giải độc lập có ghi nguồn tham khảo Bitcoin Magazine; **không tái sử dụng nguyên ảnh infographic gốc**.
