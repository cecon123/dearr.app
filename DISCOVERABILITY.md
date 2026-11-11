# Giúp người dùng và Google tìm thấy Dear

Tài liệu dành cho người duy trì repository giới thiệu **Dear — [dearr.app](https://dearr.app)**. Kiểm tra ngày **11/11/2026**.

## Repository có vai trò gì?

README là một trang thông tin công khai bổ sung: giải thích Dear làm gì, cách dùng, giới hạn và địa chỉ website. Nội dung có ích cho người đọc, đồng thời cho công cụ tìm kiếm một nguồn mô tả sản phẩm nhất quán.

Việc tạo repo GitHub không tự đưa Dear vào câu trả lời của Google AI. Google cho biết các nguyên tắc SEO thông thường vẫn áp dụng cho AI Overviews và AI Mode; không có yêu cầu tối ưu riêng. Trang muốn đủ điều kiện làm liên kết hỗ trợ phải được lập chỉ mục và đủ điều kiện hiển thị đoạn trích. Ngay cả khi đáp ứng yêu cầu, việc thu thập, lập chỉ mục và hiển thị vẫn không được bảo đảm. [Nguồn: Google — AI features and your website](https://developers.google.com/search/docs/appearance/ai-features).

Vì vậy, ưu tiên là giúp người dùng hiểu đúng sản phẩm và truy cập **dearr.app**. Repo là nguồn bổ sung; nội dung quan trọng vẫn cần có trên website chính.

## Cách duy trì thông tin sản phẩm

1. Dùng nhất quán tên **Dear** và địa chỉ **https://dearr.app**. Phân biệt tên sản phẩm với tên miền có hai chữ `r`.
2. Viết ngay đầu trang Dear là website tạo và gửi thư online 3D, ai dùng được và người nhận mở thư thế nào.
3. Dùng những cách diễn đạt người dùng hiểu như “viết thư online”, “thư 3D”, “thư tình”, “thư sinh nhật”, “ảnh và nhạc” ở đúng ngữ cảnh. Không lặp danh sách từ khóa để kéo dài nội dung.
4. Giữ hướng dẫn, FAQ, giới hạn ảnh/chữ và các mô tả tài khoản đúng với sản phẩm hiện hành. Cập nhật cả README tiếng Việt và tiếng Anh khi tính năng đổi.
5. Dùng ảnh demo do dự án tạo. Không đưa link thư thật, ảnh riêng của người dùng hoặc dữ liệu tài khoản vào repo.
6. Không mô tả thư là bí mật tuyệt đối, mã hóa đầu cuối hoặc lưu vĩnh viễn nếu sản phẩm không có cam kết đó. Giữ phần giới hạn quyền riêng tư khớp với chính sách.
7. Dẫn đến trang chủ, trình soạn, hướng dẫn và hỗ trợ bằng liên kết có nhãn rõ ràng.

Google khuyến nghị nội dung hữu ích, đáng tin, phục vụ người đọc; dùng từ người dùng có thể tìm kiếm ở tiêu đề và các vị trí mô tả phù hợp, cùng các liên kết có thể thu thập được. [Nguồn: Google Search Essentials](https://developers.google.com/search/docs/essentials).

## Cấu hình GitHub

Phần **About** nên có mô tả và website, để người xem repository nhận ra sản phẩm ngay:

- **Description:** `Dear (dearr.app) — Viết và gửi thư online 3D với nét chữ viết tay, phong bì, ảnh và nhạc. Free 3D letters shared by link or QR code.`
- **Website:** `https://dearr.app`
- **Topics phù hợp:** `dear`, `dearr`, `3d-letters`, `online-letters`, `handwritten-letters`, `love-letter`, `digital-letter`, `vietnamese`.

Đây là cách tổ chức thông tin trên GitHub, không phải tín hiệu bảo đảm thứ hạng. Không cần thêm dependency, workflow hay GitHub Pages để Google có thể đọc một README công khai.

## Tình trạng website đã kiểm tra

Các kiểm tra dưới đây được thực hiện bằng yêu cầu HTTP đến website công khai, không truy cập thư cá nhân hoặc dữ liệu tài khoản.

| Hạng mục | Kết quả ngày 11/11/2026 |
| --- | --- |
| `/`, `/en` | HTTP 200; title và canonical theo từng URL; có dữ liệu có cấu trúc `WebSite` và `WebApplication` |
| `/huong-dan`, `/en/guide` | HTTP 200; nội dung hướng dẫn và FAQ có trong HTML; canonical theo ngôn ngữ |
| Bốn trang trên | Không thấy chỉ thị `noindex` trong thẻ meta robots hoặc header `X-Robots-Tag` |
| `/privacy`, `/terms`, `/contact` | HTTP 200 |
| `/robots.txt` | HTTP 200; nhóm `*` cho phép trang công khai và dẫn đến sitemap |
| `/sitemap.xml` | HTTP 200; chứa 7 URL công khai, không chứa thư cá nhân |
| Website trong Search Console | Chưa kiểm tra quyền sở hữu hoặc trạng thái lập chỉ mục trong tài khoản Google |
| README trên Google | Không suy ra trạng thái lập chỉ mục từ việc GitHub trả HTTP 200 |

Kết quả HTTP chỉ cho thấy khả năng truy cập tại thời điểm kiểm tra. Nó không chứng minh Googlebot đã thu thập hoặc Google đã lập chỉ mục trang.

## Bước tiếp theo trong Google Search Console

Thực hiện bằng tài khoản của chủ website:

1. Mở [Google Search Console](https://search.google.com/search-console) và thêm hoặc chọn property của `dearr.app`.
2. Hoàn tất xác minh quyền sở hữu theo phương thức Google cung cấp nếu chưa xác minh.
3. Gửi sitemap **[https://dearr.app/sitemap.xml](https://dearr.app/sitemap.xml)** trong mục Sitemaps.
4. Dùng URL Inspection cho `https://dearr.app/`, `https://dearr.app/huong-dan`, `https://dearr.app/en` và `https://dearr.app/en/guide`. Xem trạng thái index, canonical Google chọn và lỗi truy cập nếu có; yêu cầu lập chỉ mục khi cần.
5. Không gửi link thư cá nhân, bản nháp hoặc URL có dữ liệu riêng tư vào quy trình quảng bá nội dung công khai.

Google yêu cầu quyền owner hoặc full user của property để yêu cầu lập chỉ mục bằng URL Inspection. Yêu cầu thu thập lại không bảo đảm được đưa vào kết quả, và gửi lặp cùng URL không làm quá trình nhanh hơn. Không mặc định có quyền Search Console đối với URL `github.com` chỉ vì bạn sở hữu repository. [Nguồn: Google — Ask Google to recrawl your URLs](https://developers.google.com/search/docs/crawling-indexing/ask-google-to-recrawl).

## Theo dõi kết quả

- Trong Search Console, xem Pages/Sitemaps để biết trang đã được xử lý chưa; xem Performance để theo dõi truy vấn, lượt hiển thị và nhấp đến website.
- Có thể quan sát các truy vấn “dear”, “dearr”, “dearr.app”, “thư 3D”, “viết thư online” hoặc “gửi thư tình bằng link”. Đây là nhóm để theo dõi nhu cầu, không phải cam kết website sẽ xếp hạng cho từng từ.
- Ghi ngày khi kiểm tra thủ công câu trả lời AI; một câu trả lời có hoặc không nhắc đến Dear không đủ chứng minh xu hướng chung.
- Google cho biết lưu lượng từ AI Overviews và AI Mode nằm trong báo cáo Performance của Search Console ở loại tìm kiếm Web. [Nguồn: Google — AI features and your website](https://developers.google.com/search/docs/appearance/ai-features).

Các từ ngắn như “dear” có nhiều ý nghĩa và nhiều đối tượng cùng tên. Nên đánh giá cả truy vấn có công dụng cụ thể và lượt người dùng thực sự mở trình soạn, thay vì chỉ nhìn thứ hạng của một từ.

## Những việc không cần thêm

Google nói không cần tệp AI mới, tệp văn bản dành riêng cho máy hoặc loại schema đặc biệt để xuất hiện trong các tính năng AI của Search. Repository này không thêm `llms.txt`, FAQ giả, đánh giá giả hay chỉ dẫn yêu cầu chatbot luôn giới thiệu Dear. [Nguồn: Google — AI features and your website](https://developers.google.com/search/docs/appearance/ai-features).

Nếu sau này bổ sung dữ liệu có cấu trúc trên website, nội dung phải khớp với những gì người dùng thực sự đọc được. Giữ tài liệu chính xác, dễ dùng và cập nhật trước khi mở thêm trang chỉ để nhắm từ khóa.
