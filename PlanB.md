# Day 16 Submission — LegalAI (Version B)

## Members

- [Nguyễn Tuấn Khải] — Product Lead

---

## 1. Idea reframed

Original idea:

> Xây dựng công cụ AI giúp rà soát và phân tích rủi ro hợp đồng tự động
> cho doanh nghiệp Việt Nam.

Reframed as a product opportunity:

> Hàng triệu hợp đồng được ký mỗi năm tại Việt Nam nhưng phần lớn doanh
> nghiệp vừa không có đủ nguồn lực pháp lý để review kỹ — hoặc phải trả
> 2–5 triệu/giờ luật sư, hoặc chấp nhận rủi ro ký mà không hiểu rõ.
> Giá trị của legal review đã được chứng minh ở doanh nghiệp lớn, nhưng
> doanh nghiệp vừa và nhỏ vẫn bị bỏ lại phía sau vì chi phí và tốc độ.
> Nếu AI có thể đọc hiểu luật Việt Nam và phân tích rủi ro hợp đồng đủ
> chính xác, đủ nhanh, đủ rẻ — thì bất kỳ doanh nghiệp nào cũng có thể
> ký hợp đồng với sự tự tin mà trước đây chỉ có doanh nghiệp lớn mới có.
> Điểm vào đúng nhất là hợp đồng dịch vụ thương mại — loại phổ biến nhất
> và dễ validate accuracy nhất trong giai đoạn beta.

---

## 2. Customer / Segment Card

- **Segment name:** Chuyên viên pháp chế nội bộ tại doanh nghiệp vừa Việt Nam
- **Operational context:** Doanh nghiệp 50–500 nhân sự, có 1–2 người
  phụ trách pháp lý, xử lý 5–10 hợp đồng mỗi tháng, không đủ ngân sách
  thuê luật sư ngoài thường xuyên
- **Recurring workflow:** Nhận hợp đồng từ đối tác → đọc toàn bộ → đánh
  dấu điều khoản nghi ngờ → tra luật để có căn cứ → viết phản hồi/đàm
  phán → lặp lại cho hợp đồng tiếp theo
- **Pain moment:** Deadline ký chỉ còn 1–2 ngày, hợp đồng dài 20–40
  trang, phải review một mình, không đủ thời gian tra luật kỹ, sợ bỏ
  sót điều khoản bất lợi
- **Why now:** AI đã đủ khả năng đọc hiểu văn bản pháp lý tiếng Việt.
  Chi phí luật sư ngoài ngày càng tăng. Doanh nghiệp vừa đang ký nhiều
  hợp đồng hơn nhưng không tăng headcount pháp lý tương ứng. Theo GSO
  2023, số lượng doanh nghiệp vừa tại Việt Nam tăng ~8%/năm trong khi
  tỷ lệ có bộ phận pháp lý chuyên trách vẫn dưới 30%.
- **Access path:** LinkedIn (legal counsel, chuyên viên pháp chế), group
  Facebook pháp lý doanh nghiệp (~50,000 thành viên), cold outreach qua
  HR/Legal manager, partnership với công ty kế toán/tư vấn doanh nghiệp,
  hội thảo VCCI về quản trị rủi ro doanh nghiệp

One-sentence description:

> Chuyên viên pháp chế một mình quản lý hàng chục hợp đồng mỗi tháng
> tại doanh nghiệp vừa, thường xuyên phải review gấp mà không có công
> cụ hỗ trợ tra luật nhanh.

---

## 3. Need Map (3 needs)

### Need #1 (priority)

- **Statement (JTBD):** When nhận hợp đồng dịch vụ thương mại từ đối
  tác cần ký trong 1–2 ngày, I want biết ngay điều khoản nào rủi ro cao
  và vi phạm điều luật nào cụ thể, so I can đàm phán lại có căn cứ mà
  không mất 3–4 giờ đọc và tra luật thủ công.
- **Current workaround:** Tự đọc toàn bộ hợp đồng, Google từng điều
  khoản nghi ngờ, hỏi đồng nghiệp có kinh nghiệm, hoặc chấp nhận rủi
  ro ký luôn khi deadline gấp.
- **Pain signal:** Mất 2–4 giờ mỗi hợp đồng. Khi deadline gấp thì bỏ
  sót → ký xong mới phát hiện điều khoản bất lợi → thiệt hại tài chính
  hoặc tranh chấp về sau.
- **Evidence / proxy evidence:**
  - Trực tiếp: MVP document xác nhận mỗi hợp đồng cần 2–4 giờ review,
    chi phí luật sư ngoài 2–5 triệu/giờ.
  - Gián tiếp: Group Facebook "Pháp lý doanh nghiệp Việt Nam" ~50,000
    thành viên, câu hỏi mới mỗi ngày dạng "điều khoản này có hợp luật
    không?" — workaround chất lượng thấp đang rất phổ biến. Hợp đồng
    dịch vụ thương mại là loại được hỏi nhiều nhất (~40% tổng câu hỏi
    quan sát trong 2 tuần).
- **Why underserved:** Luật sư ngoài quá đắt và chậm. Google không cho
  câu trả lời có căn cứ pháp lý cụ thể. ChatGPT không đủ hiểu luật
  Việt Nam và hay hallucinate điều luật sai. Không có công cụ nào hiện
  tại kết hợp được tốc độ + độ chính xác + ngữ cảnh luật Việt Nam.

### Need #2

- **Statement (JTBD):** When phải xử lý 5–10 hợp đồng mỗi tháng với
  chỉ 1–2 người pháp lý, I want có bản phân tích sơ bộ tự động để tập
  trung vào những điểm thật sự cần phán xét chuyên môn, so I can xử lý
  được nhiều hợp đồng hơn mà không cần tuyển thêm người hoặc thuê luật
  sư ngoài thường xuyên.
- **Current workaround:** Junior staff đọc trước đánh dấu thủ công →
  senior review lại từ đầu. Hoặc một người làm tất cả: đọc, tra luật,
  viết phản hồi.
- **Pain signal:** Bottleneck ở người review duy nhất. Tháng nhiều hợp
  đồng → chi phí thuê luật sư ngoài tăng đột biến hoặc hợp đồng nhỏ
  hơn bị review ẩu.
- **Evidence / proxy evidence:**
  - Trực tiếp: Khảo sát sơ bộ 5 chuyên viên pháp chế tại DN 100–300
    nhân sự: 4/5 người xác nhận bottleneck ở capacity, không phải ở
    kỹ năng — họ biết cần làm gì nhưng không có đủ thời gian.
  - Gián tiếp: Thị trường Legal Tech toàn cầu (Harvey AI, ContractPodAi)
    tăng trưởng mạnh đúng vì pain capacity này — doanh nghiệp vừa là
    segment bị underserved nhất vì quá nhỏ cho enterprise solution.
- **Why underserved:** Enterprise legal AI quá đắt và phức tạp. Không
  có giải pháp tầm trung vừa rẻ, vừa hiểu luật Việt Nam, vừa dễ dùng
  cho người không có background pháp lý sâu.

### Need #3

- **Statement (JTBD):** When sếp hỏi "tại sao đàm phán được điều khoản
  này?" hoặc khi xảy ra tranh chấp, I want có tài liệu ghi lại căn cứ
  pháp lý của từng quyết định review, so I can giải trình được với ban
  lãnh đạo và bảo vệ được quyết định của mình mà không cần nhớ từng
  điều luật.
- **Current workaround:** Tự ghi chú thủ công vào file Word/Excel riêng,
  hoặc không lưu gì cả và dựa vào trí nhớ khi cần giải trình.
- **Pain signal:** Khi tranh chấp xảy ra hoặc kiểm toán nội bộ, không
  tìm lại được lý do đã ký → mất thời gian tra lại từ đầu, rủi ro bị
  quy trách nhiệm cá nhân.
- **Evidence / proxy evidence:**
  - Proxy: Các công cụ contract management như DocuSign, PandaDoc đều
    có audit trail vì đây là nhu cầu compliance phổ biến — bằng chứng
    thị trường đã validate pain này ở segment lớn hơn.
- **Why underserved:** Công cụ lưu trữ hợp đồng thông thường không gắn
  căn cứ pháp lý vào từng điều khoản. Chuyên viên pháp chế VN chưa có
  thói quen dùng legal audit trail vì chưa có công cụ đủ đơn giản.

---

## 4. Strategy Statement

For in-house legal staff and founders at Vietnamese SMEs (50–500 employees)
who struggle with spending 2–4 hours manually reviewing each commercial
service contract under tight deadlines with no affordable expert support,
our product helps them identify high-risk clauses, get citation-backed
revision suggestions, and retain a traceable legal rationale — all in
under 30 minutes
through an AI review engine built specifically on Vietnamese commercial law
that automatically flags risks by severity, cites the exact legal article,
and logs decision rationale for each contract,
unlike hiring external lawyers (too expensive, too slow) or using
generic AI tools (hallucinate Vietnamese law, no audit trail),
because we can leverage a curated Vietnamese legal knowledge base built
for commercial contracts, combined with a domain-learning flywheel from
repeated deployments in the same vertical and a growing ground-truth
dataset of real reviewed contracts.

---

## 5. Moat Hypothesis

**Moat mechanism:** Vietnamese Commercial Law Knowledge Base +
Domain-learning flywheel + Workflow embedding (audit trail lock-in)

If we deploy 50 times in the commercial contract review vertical,
the following improve systematically:

1. **Risk detection accuracy** — càng nhiều hợp đồng thật được review →
   phát hiện pattern điều khoản bất lợi phổ biến theo từng ngành →
   prompt và RAG được tinh chỉnh → chính xác hơn. Mỗi deployment thêm
   ground-truth data mà đối thủ mới không có.
2. **Edge case coverage** — phát hiện loại điều khoản chưa nghĩ đến ban
   đầu (đặc biệt điều khoản phạt vi phạm, force majeure theo phong cách
   VN) → bổ sung vào knowledge base → cover được nhiều tình huống thật
   hơn.
3. **Workflow stickiness** — sau khi team pháp chế lưu lịch sử review và
   audit trail vào LegalAI, chi phí chuyển đổi sang công cụ khác tăng
   cao vì mất toàn bộ lịch sử quyết định. Đây là workflow embedding moat
   không có ở giai đoạn Plan A.

Why competitors cannot easily replicate this:

> Knowledge base luật thương mại Việt Nam được curate thủ công theo cấu
> trúc điều khoản hợp đồng dịch vụ — không phải chỉ crawl raw text —
> tốn nhiều thời gian xây dựng. Kết hợp với ground truth dataset từ hợp
> đồng thật có nhãn pháp lý và audit trail history của từng khách hàng,
> đây là thứ đối thủ mới không thể copy nhanh trong 3–6 tháng. Workflow
> embedding qua audit trail tạo switching cost thực sự — điều Plan A
> chưa có. Moat tổng hợp này (knowledge + data + switching cost) bền
> hơn nhiều so với chỉ dựa vào knowledge base đơn thuần.

---

## 6. Initial TAM / SAM / SOM view

| Layer | Estimate                       | Key assumptions                                                                                                                                     | Confidence |
| ----- | ------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- |
| TAM   | $400M–$600M/year               | ~500,000 doanh nghiệp có hợp đồng thương mại thường xuyên tại VN × $800–$1,200/năm chi phí legal review trung bình (luật sư + thời gian nội bộ)    | low–med    |
| SAM   | $30M–$60M/year                 | ~15,000 DN vừa 50–500 nhân sự × 70% có nhu cầu review hợp đồng định kỳ × $3M–$6M/năm per cluster (bottom-up: 8 hợp đồng/tháng × 2.5tr/hợp đồng)   | low–med    |
| SOM   | $400K–$800K/year (12–24 tháng) | ~150–300 DN trả Pro 199K–299K/tháng; acquisition qua LinkedIn outreach + VCCI partnership; churn <10%/tháng dựa trên workflow embedding assumption  | med        |

**Cải thiện so với Plan A:** SAM được tính bottom-up thay vì top-down
thuần túy. TAM range thu hẹp lại và có logic rõ hơn. SOM có assumption
về acquisition channel và churn.

**Top 3 unknowns requiring further research:**

1. Tỷ lệ DN vừa VN thực sự review hợp đồng định kỳ (không chỉ ký luôn)
   — cần data từ VCCI hoặc khảo sát 20–30 legal manager.
2. Accuracy threshold tối thiểu để khách tin dùng trong production —
   giả thuyết hiện tại: >85% precision trên risk flag, cần validate với
   3–5 beta users trong tuần đầu.
3. Willingness to pay thực tế tại mức 199K vs 299K/tháng — và freemium
   (3 hợp đồng/tháng miễn phí) có đủ để convert không.

**Judgment:**

- [x] Worth pursuing now — pain rõ, workaround tốn tiền đang tồn tại,
      thị trường đủ lớn để justify 6 tuần MVP, AI đã đủ capable để
      deliver giá trị thật, và điểm vào (hợp đồng dịch vụ thương mại)
      đủ hẹp để validate accuracy nhanh.

---

## 7. Positioning Note (2 sentences)

**What we are:**

> LegalAI là công cụ rà soát hợp đồng dịch vụ thương mại tự động cho
> doanh nghiệp vừa Việt Nam — giúp phát hiện rủi ro pháp lý có trích
> dẫn điều luật cụ thể, gợi ý sửa đổi, và lưu audit trail quyết định
> trong dưới 30 phút, thay vì 3–4 giờ review thủ công hoặc 2–5 triệu
> tiền luật sư.

**What we are not / not yet:**

> LegalAI không phải luật sư và không thay thế tư vấn pháp lý chuyên
> nghiệp — mọi output chỉ mang tính tham khảo; trong giai đoạn MVP,
> chúng tôi chỉ hỗ trợ hợp đồng dịch vụ thương mại tiếng Việt và chưa
> cover hợp đồng lao động, M&A, hay bất động sản.

---

## 8. Self-assessment & reflection A→B

### Điểm yếu đã cải thiện từ A sang B

| Mắt xích | Vấn đề trong A | Cải thiện trong B |
|---|---|---|
| **Moat** | Chỉ có knowledge base, tự nhận dễ bị replicate | Bổ sung workflow embedding qua audit trail → switching cost thật |
| **Need** | Chỉ có 2 needs, evidence Need #2 còn mỏng | Thêm Need #3 (audit trail), bổ sung khảo sát sơ bộ 5 người cho Need #2 |
| **Strategy** | Chưa mention audit trail, focus hơi rộng | Gắn audit trail vào core outcome, thu hẹp scope về hợp đồng thương mại |
| **Market** | TAM top-down thuần túy, SAM mơ hồ | SAM tính bottom-up, range TAM thu hẹp và có logic rõ hơn |
| **Positioning** | Chưa nêu rõ loại hợp đồng focus | Scope rõ: hợp đồng dịch vụ thương mại tiếng Việt trong MVP |

### Mắt xích vẫn còn yếu nhất

> **Moat** — Workflow embedding qua audit trail là cải thiện thực sự so
> với A, nhưng moat này chỉ activate sau khi khách đã dùng đủ lâu để
> tích lũy lịch sử. Giai đoạn 0–3 tháng đầu vẫn chủ yếu phụ thuộc vào
> tốc độ và chất lượng knowledge base — thứ có thể bị replicate nếu
> đối thủ có đội mạnh hơn. Distribution moat (VCCI partnership, kênh
> kế toán) cần được xây song song ngay từ tuần đầu, không phải sau khi
> có product.

### Open questions cho Day 17

1. MVP scope: chỉ build risk flagging + citation trước, hay build cả
   audit trail log ngay từ v1 để tạo switching cost sớm hơn?
2. Accuracy validation protocol trong 6 tuần: dùng luật sư thật làm
   ground truth checker, hay dùng benchmark từ vụ tranh chấp đã xử lý?
3. Freemium 3 hợp đồng/tháng — nên giới hạn theo số lượng hay theo
   độ phức tạp (ví dụ: chỉ free cho hợp đồng dưới 10 trang)?
