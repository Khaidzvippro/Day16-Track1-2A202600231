# Day 16 Submission — LegalAI

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
  hợp đồng hơn nhưng không tăng headcount pháp lý tương ứng.
- **Access path:** LinkedIn (legal counsel, chuyên viên pháp chế), group
  Facebook pháp lý doanh nghiệp, cold outreach qua HR/Legal manager,
  partnership với công ty kế toán/tư vấn doanh nghiệp

One-sentence description:

> Chuyên viên pháp chế một mình quản lý hàng chục hợp đồng mỗi tháng
> tại doanh nghiệp vừa, thường xuyên phải review gấp mà không có công
> cụ hỗ trợ tra luật nhanh.

---

## 3. Need Map (2 needs)

### Need #1 (priority)

- **Statement (JTBD):** When nhận hợp đồng từ đối tác cần ký trong 1–2
  ngày, I want biết ngay điều khoản nào rủi ro cao và vi phạm luật nào
  cụ thể, so I can đàm phán lại có căn cứ mà không mất 3–4 giờ đọc và
  tra luật thủ công.
- **Current workaround:** Tự đọc toàn bộ hợp đồng, Google từng điều
  khoản nghi ngờ, hỏi đồng nghiệp có kinh nghiệm, hoặc chấp nhận rủi
  ro ký luôn khi deadline gấp.
- **Pain signal:** Mất 2–4 giờ mỗi hợp đồng. Khi deadline gấp thì bỏ
  sót → ký xong mới phát hiện điều khoản bất lợi → thiệt hại tài chính
  hoặc tranh chấp về sau.
- **Evidence / proxy evidence:**
  - Trực tiếp: MVP document xác nhận mỗi hợp đồng cần 2–4 giờ review,
    chi phí luật sư ngoài 2–5 triệu/giờ.
  - Gián tiếp: Group Facebook pháp lý doanh nghiệp VN hàng chục nghìn
    thành viên, câu hỏi mới mỗi ngày dạng "điều khoản này có hợp luật
    không?" — workaround chất lượng thấp đang rất phổ biến.
- **Why underserved:** Luật sư ngoài quá đắt và chậm. Google không cho
  câu trả lời có căn cứ pháp lý cụ thể. ChatGPT không đủ hiểu luật
  Việt Nam và hay hallucinate điều luật sai.

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
  - Trực tiếp: MVP document xác nhận Persona 1 — doanh nghiệp vừa
    50–500 nhân sự, 5–10 hợp đồng/tháng, bị hạn chế bởi thời gian.
  - Gián tiếp: Thị trường Legal Tech toàn cầu (Harvey AI, ContractPodAi)
    tăng trưởng mạnh đúng vì pain capacity này — doanh nghiệp vừa là
    segment bị underserved nhất vì quá nhỏ cho enterprise solution.
- **Why underserved:** Enterprise legal AI quá đắt và phức tạp. Không
  có giải pháp tầm trung vừa rẻ, vừa hiểu luật Việt Nam, vừa dễ dùng
  cho người không có background pháp lý sâu.

---

## 4. Strategy Statement

For in-house legal staff and founders at Vietnamese SMEs (50–500 employees)
who struggle with spending 2–4 hours manually reviewing each contract
under tight deadlines with no affordable expert support,
our product helps them identify high-risk clauses and get
citation-backed revision suggestions in under 30 minutes
through an AI review engine built on Vietnamese law that automatically
flags risks by severity and cites the exact legal article,
unlike hiring external lawyers (too expensive, too slow) or using
generic AI tools (hallucinate Vietnamese law),
because we can leverage a curated Vietnamese legal knowledge base
built specifically for contract review, combined with a domain-learning
flywheel from repeated deployments in the same vertical.

---

## 5. Moat Hypothesis

**Moat mechanism:** Vietnamese Law Knowledge Base +
Domain-learning flywheel

If we deploy 50 times in the contract review vertical, the following
improve systematically:

1. Risk detection accuracy — càng nhiều hợp đồng thật được review →
   phát hiện pattern điều khoản bất lợi phổ biến theo từng ngành →
   prompt và RAG được tinh chỉnh → chính xác hơn.
2. Edge case coverage — phát hiện loại điều khoản chưa nghĩ đến ban
   đầu → bổ sung vào knowledge base → cover được nhiều tình huống thật
   hơn.
3. Onboarding speed — hiểu sâu workflow review của doanh nghiệp VN →
   setup nhanh hơn → khách dùng được ngay mà không cần cấu hình phức
   tạp.

Why competitors cannot easily replicate this:

> Knowledge base luật Việt Nam được curate thủ công theo cấu trúc điều
> khoản — không phải chỉ crawl raw text — tốn nhiều thời gian xây dựng.
> Kết hợp với ground truth dataset từ hợp đồng thật có nhãn pháp lý,
> đây là thứ đối thủ mới không thể copy nhanh trong 3–6 tháng. Tuy
> nhiên, moat này chỉ thật sự mạnh sau khi có 30–50 deployments thật —
> giai đoạn đầu lợi thế chủ yếu đến từ tốc độ và quan hệ khách hàng
> đầu tiên.

---

## 6. Initial TAM / SAM / SOM view

| Layer | Estimate                     | Key assumptions                                                                                  | Confidence |
| ----- | ---------------------------- | ------------------------------------------------------------------------------------------------ | ---------- |
| TAM   | $500M–$1B/year               | Toàn bộ thị trường legal services VN, bao gồm luật sư, công ty luật, legal review nội bộ         | low        |
| SAM   | $50M–$100M/year              | Doanh nghiệp vừa 50–500 nhân sự tại VN (~15,000 DN), mỗi DN chi 3–5 triệu/tháng cho legal review | low–med    |
| SOM   | $500K–$1M/year (12–24 tháng) | Chiếm 1–2% SAM, ~200–300 doanh nghiệp trả Pro 199K/tháng                                         | med        |

**Top 3 unknowns requiring further research:**

1. Số lượng doanh nghiệp vừa VN thực sự có nhu cầu review hợp đồng
   thường xuyên — cần khảo sát hoặc tìm data từ VCCI, GSO.
2. Willingness to pay thực tế — 199K/tháng có đủ thấp để thử không,
   hay cần freemium mạnh hơn để convert.
3. Mức độ chính xác tối thiểu khách hàng chấp nhận — nếu AI sai 1
   điều luật thì khách có còn tin không.

**Judgment:**

- [x] Worth pursuing now — pain rõ, workaround tốn tiền đang tồn tại,
      thị trường đủ lớn để justify 6 tuần MVP, và AI đã đủ capable để
      deliver giá trị thật.

---

## 7. Positioning Note (2 sentences)

**What we are:**

> LegalAI là công cụ rà soát hợp đồng tự động cho doanh nghiệp Việt
> Nam — giúp phát hiện rủi ro pháp lý có trích dẫn điều luật cụ thể
> trong dưới 30 phút, thay vì 3–4 giờ review thủ công hoặc 2–5 triệu
> tiền luật sư.

**What we are not / not yet:**

> LegalAI không phải luật sư và không thay thế tư vấn pháp lý chuyên
> nghiệp — mọi output chỉ mang tính tham khảo, và chúng tôi chưa hỗ
> trợ collaboration nhiều người, diff tracking, hay API enterprise trong
> giai đoạn MVP này.

---

## 8. Self-assessment before Day 17

Trong 6 mắt xích (Idea → Customer → Need → Strategy → Moat → Market
Size), mắt xích đang yếu nhất là:

> **Moat** — Lợi thế cạnh tranh của LegalAI giai đoạn đầu chưa thật
> sự bền. Knowledge base luật VN có thể bị đối thủ replicate nếu họ
> có đội mạnh hơn. Moat thật sự chỉ đến từ 30–50 deployments đầu tiên
> và quan hệ với khách hàng thật — thứ chưa có trong tay lúc này.
> Cần nghĩ thêm về distribution moat hoặc workflow embedding sau MVP.

Open questions muốn khám phá thêm ở Day 17:

1. MVP nên focus hợp đồng lao động hay hợp đồng dịch vụ thương mại
   trước — loại nào dễ validate accuracy hơn trong 6 tuần?
2. Accuracy threshold tối thiểu để khách hàng tin dùng là bao nhiêu —
   và làm sao đo được trong giai đoạn beta?
3. Freemium 3 hợp đồng/tháng có đủ để khách trải nghiệm giá trị thật
   trước khi quyết định trả tiền không?
