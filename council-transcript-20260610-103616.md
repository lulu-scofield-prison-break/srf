# Council Transcript — SRF IaaS Internal Training Guide
> Phiên council · 2026-06-10 10:36 · counciled: `srf_iaas_training_guide.md`

---

## Câu Hỏi Gốc
"/llm-council review bản này" — review tài liệu `srf_iaas_training_guide.md`.

---

## Câu Hỏi Đã Được Frame
Review tài liệu **"SRF IaaS Team — Internal Training Guide"** (playbook nội bộ cho team Farm Solutions Group / FSG bán & support sản phẩm IaaS rental mới của Super Renders Farm).

Bối cảnh: SRF historically là managed SaaS render farm (client upload scene → SRF render → client download). Đây là pivot/mở rộng sang **IaaS** — cho thuê dedicated node 24/7, client tự chạy pipeline, tính flat rate per node block. Tài liệu codify: team structure (Solutions Lead / Render Engineer / FSG Coordinator), pricing reference (CPU Xeon nodes + GPU RTX 5090 machines), pre-sales playbook 5 bước, support procedures (onboarding D-7→Day1, active render SLA), và **1 case study** — Adcetera #33493: 18x RTX 5090, 3 tuần, $25,500; deal suýt vỡ vì một rough estimate $10k blow up ~80% nhưng được cứu nhờ owning mistake + offer Yearly Capacity Lock.

**Câu hỏi:** Tài liệu này — và chiến lược go-to-market IaaS mà nó encode — có vững không? Có nên roll out cho team như hiện tại không? Pressure-test từ mọi góc và recommend.

> **Lưu ý vận hành:** Phiên này chạy trong môi trường chat (single-context council), không phải sub-agent song song của Claude Code. 5 lens được embody độc lập + peer review ẩn danh + chairman synthesis, theo đúng pattern của skill.

---

## Bảng Anonymize
| Letter | Advisor |
|--------|---------|
| A | Người Mở Rộng (The Expansionist) |
| B | Người Phản Biện (The Contrarian) |
| C | Người Thực Thi (The Executor) |
| D | Người Ngoài Cuộc (The Outsider) |
| E | Tư Duy Gốc (The First Principles Thinker) |

---

## Phản Hồi Cố Vấn

### Phản Hồi A — Người Mở Rộng (The Expansionist)
Mọi người sẽ soi pricing sai chỗ này chỗ kia. Tôi thấy cơ hội lớn hơn nhiều đang nằm ngay trước mắt mà tài liệu bỏ lỡ.

Adcetera không phải một deal — nó là beachhead của cả một category. Câu *"We also do 5–6 of these shows a year. We currently use Rebus in Germany but were hoping for a better solution"* là vàng. Có cả một segment broadcast/event studio: production lặp lại, deadline cứng, đang kẹt với provider châu Âu, coi certainty quan trọng hơn giá, và SẴN SÀNG ký cam kết năm. Yearly Capacity & Price Lock không phải upsell — nó là sản phẩm chính. SRF nên lật model: lead bằng annual capacity subscription, không phải one-off rental. One-off chỉ là trial; annual lock mới là business — và nó biến IaaS từ doanh thu lumpy, khó dự báo thành ARR forecastable, đồng thời giải bài toán cannibalization (lên kế hoạch pool theo committed capacity).

LucidLink/Suite Studios bị tài liệu coi là "integration để mention". Sai. Đó là moat. Nếu SRF là render target mount thẳng vào filespace có sẵn của studio — không re-upload, môi trường pre-configured — SRF ngừng cạnh tranh giá render và trở thành hạ tầng mà pipeline của studio phụ thuộc vào. High switching cost, defensible.

Và bản thân case study Adcetera (deal suýt vỡ được cứu bằng sự trung thực) — anonymized — là content marketing tuyệt vời cho đúng segment cao cấp SRF đang nhắm. Đừng chôn nó làm bài học nội bộ. Nó là external gold.

Rủi ro lớn nhất ở đây không phải mấy con số sai — mà là nghĩ quá nhỏ.

### Phản Hồi B — Người Phản Biện (The Contrarian)
Đây không phải training guide — nó là post-mortem mặc áo playbook. Và nó sẽ tạo RA thêm "cú sốc Adcetera", không ngăn được.

Thứ nhất: toàn bộ playbook xây trên n=1. Adcetera là một deal — một deal suýt vỡ rồi được cứu. Codify "best practice" từ một mẫu duy nhất, lại là near-miss, là cực kỳ rủi ro. $25,500 được coi là "calibration reference" nhưng nó chỉ là một director-approved floor dưới áp lực deadline. Đó không phải pricing model, đó là giai thoại.

Thứ hai — và đây là vấn đề chí mạng: pricing TỰ MÂU THUẪN. Rate IaaS published: 1 GPU machine (2x RTX 5090) = $1,172.50/tuần. Adcetera "18x RTX 5090 machines", 3 tuần = $25,500. 18 × $1,172.50 × 3 = **$63,315** — gấp ~2.5 lần deal thật. Một rep KHÔNG THỂ tái tạo $25,500 từ bảng giá. Tệ hơn: rule #3 nói *"rate doesn't scale linearly"*, nhưng ví dụ đưa ra để chứng minh ($17k / $25.5k / $34k) lại **tuyến tính hoàn hảo** — đúng $8,500/tuần mỗi mốc. Tài liệu mâu thuẫn với chính nó trong cùng một mục. Đưa cái này cho team = đảm bảo mỗi rep đẻ ra một con số khác nhau.

Thứ ba: cái "fix" thật ra là band-aid. Root cause Adcetera không phải thiếu caveat — mà là rep đưa estimate sai 80%. Một câu disclaimer không sửa được estimate sai; nó chỉ xin lỗi trước. Fix thật: đừng đưa số cho đến khi đưa được số defensible.

Thứ tư: 24/7, SLA 1 giờ, uptime 99.9% — team ở Hanoi, client US/EU render ban đêm giờ Hanoi. Ai trực SLA 1 giờ lúc 3 giờ sáng? Không có coverage plan. SLA không giữ được = sự cố phá vỡ niềm tin tiếp theo. Và "consider SLA credit" — credit bao nhiêu? Không định nghĩa = client tự định nghĩa giúp bạn, ngay giữa lúc nóng.

Sửa pricing model và coverage model TRƯỚC khi cho bất kỳ ai bán bằng tài liệu này.

### Phản Hồi C — Người Thực Thi (The Executor)
Bỏ lý thuyết — team FSG có chạy được bằng tài liệu này sáng thứ Hai không? Phần lớn là không, và đây là khoảng cách giữa "đã viết ra" và "vận hành được".

1. **Không có quote calculator.** Mỗi quote cần: check availability, áp dedicated premium, tính duration, phân biệt estimate vs quote, xin Director duyệt nếu non-standard — 5 phán đoán/quote, mà số tham chiếu lại không khớp nhau. Fix thứ Hai: dựng một sheet một trang, rep nhập (node type, count, weeks) → ra số defensible + caveat tự gắn. Chưa có nó thì rep nào cũng improvise → Adcetera lặp lại.

2. **SLA "quote trong 24h" phụ thuộc Director — mà Director là bottleneck.** Discount, duration lạ, capacity hold đều cần Director. Nếu Director cũng là một người bận (Richard?), lời hứa 24h chết ngay tuần bận đầu tiên. Fix: pre-approve một discount band + duration matrix để rep quote trong guardrail mà KHÔNG chờ Director. Chỉ giữ Director cho deal thật sự off-matrix.

3. **Onboarding D-7 → Day 1 giả định payment về đúng D-7.** Nhưng capacity chỉ lock sau payment, mà client mặc cả tới sát giờ (Adcetera đổi giá/scope vài ngày trước start). Payment về D-3 thì sao? Cửa sổ setup 5 ngày sụp. Fix: định nghĩa "compressed onboarding" + cutoff cứng ("payment chưa confirm trước D-X = không guarantee start date").

4. **SLA hardware 1 giờ cần on-call rota — tài liệu không có.** Fix: publish lịch on-call thật + runbook 3 bước RE check trước khi escalate.

5. **"Log vào CRM" — CRM nào? Field gì?** Fix: một deal-tracking template với field bắt buộc: client, node count, dates, quoted price, cờ estimate-vs-quote, Director-approved Y/N, payment status, capacity-locked Y/N.

Công bằng mà nói: intent của các procedure (paper trail, lock-after-payment, handoff) ĐÚNG — chúng vá đúng lỗ hổng Adcetera. Vấn đề là policy không có tool. Policy không tool chỉ là hy vọng. Hành động đòn bẩy cao nhất sáng thứ Hai: dựng quote calculator. Đừng để ai bán bằng guide này trước khi sheet đó tồn tại.

### Phản Hồi D — Người Ngoài Cuộc (The Outsider)
Tôi không biết SRF, không biết render. Đọc lạnh như vừa join team FSG. Đây là những chỗ tôi thấy rối:

1. **"Node", "machine", "GPU" khác nhau thế nào?** Mục CPU nói "nodes". Mục GPU nói "machines" (mỗi machine 2 GPU). Adcetera nói "18x RTX 5090 machines". Là 18 machine hay 18 GPU? Là rep mới, tôi thật sự không biết Adcetera nhận bao nhiêu thiết bị vật lý → không thể sanity-check một quote.

2. **Giá GPU trong bảng nối với deal Adcetera ở đâu?** 1 machine = $1,172.50/tuần. Adcetera "18x", 3 tuần, $25,500. Tôi nhân thử, không ra. Client hỏi "sao lại $25,500?" — tôi chịu.

3. **"33% off standard" — off cái gì?** Bảng gạch $1,750 → $1,172.50. Cái gì làm $1,750 thành "standard"? Có public chỗ nào client check được không? Nếu client Google ra rate pay-as-you-go khác $1,750, cái discount trông giả.

4. **Client nhắn "2 giờ sáng render không chạy" thì tôi LÀM GÌ?** Tài liệu nói "xác định hardware hay pipeline". OK — bằng cách nào? Check gì? Gọi ai? Escalation RE → Solutions Lead → Director, nhưng giữa đêm có ai thức? Không có on-call, không runbook.

5. **"Director" xuất hiện 6 lần nhưng không định nghĩa.** Director của gì? Một người? Liên lạc sao? Mọi deal hay ho đều cần Director duyệt mà tôi không biết Director là ai → lời hứa "quote 24h" vỡ.

6. **Vai trò chồng chéo.** Solutions Lead "owns pricing". Coordinator "logs commitments" + "sends invoices". RE làm kỹ thuật. Nhưng AI gửi quote? Ai lock capacity trong hệ thống? Client reply quote thì ai trả lời? Là người mới tôi không biết tin nhắn này thuộc ai trong ba người.

Chiến lược có thể xuất sắc, nhưng như viết hiện tại tài liệu giả định người đọc đã biết vocabulary, logic giá và org chart của SRF. Một FSG mới không thể an toàn ra quote hay xử lý sự cố 2 giờ sáng chỉ từ guide này. Mà người tự tin hành động trên hướng dẫn mơ hồ — chính xác là cách cú sốc Adcetera xảy ra ngay từ đầu.

### Phản Hồi E — Tư Duy Gốc (The First Principles Thinker)
Quên "training guide này tốt không". SRF thật sự đang cố làm gì?

Surface: "dạy team FSG bán & support IaaS". Lùi lại. Core product của SRF là managed SaaS rendering — productized, scalable, async. Bạn không nói chuyện với phần lớn khách. Margin đến từ utilization + automation. IaaS dedicated rental là NGƯỢC LẠI: high-touch, bespoke, đồng bộ thời gian thực, custom pricing từng deal. Nó là business consulting/services khoác áo infrastructure.

Nên câu hỏi thật không phải "chạy IaaS sales sao" — mà là "SRF có chắc muốn ở trong HAI business khác nhau về bản chất, và đây có phải cái đáng bolt-on không?"

Adcetera lộ ra job-to-be-done thật: một class khách (broadcast/event, 5–6 production/năm, deadline cứng, custom pipeline, đang dùng Rebus/iRender) muốn dedicated capacity guaranteed và trả premium cho CERTAINTY — không shared queue, không bất ngờ. Thứ họ mua là "sự chắc chắn dưới áp lực deadline", không phải "hardware".

Nếu vậy, tài liệu đang optimize sai layer. Nó ngập trong tactic bán (quote SLA, handoff, paper trail) mà không bao giờ định nghĩa SẢN PHẨM: "dedicated certainty" là SKU gì? Guarantee là gì? SRF fail capacity thì sao? Cả value prop là "chúng tôi đảm bảo bạn không bị burn" — nhưng không có guarantee nào được định nghĩa. SLA mơ hồ, SLA credit "consider", capacity chỉ lock sau payment (bảo vệ SRF, không phải certainty của client).

Tài liệu còn gộp hai khách khác nhau: (1) whale như Adcetera — đáng white-glove FSG; (2) khách bảng giá "5 CPU node $300/tuần" — gần như self-serve. Tại sao áp cùng một motion nặng (discovery call, formal quote, Director approval, handoff) cho một giao dịch $300? Cost-to-serve lộn ngược hoàn toàn.

Reframe: câu hỏi đúng là "chúng ta bán sản phẩm gì, cho ai, và guarantee gì?". Định nghĩa sản phẩm (một certainty SKU với SLA + capacity guarantee viết rõ) và segment motion theo deal size (self-serve cho commodity, FSG cho whale) TRƯỚC khi đánh bóng script. Training guide đang trả lời một câu hỏi SRF chưa hỏi xong.

---

## Peer Review

### Reviewer 1
1. **Mạnh nhất: E.** Response duy nhất hỏi "chúng ta bán gì, cho ai, guarantee gì" thay vì vá tactic. Quan sát "$300 CPU rental và $25k whale deal không thể dùng chung một motion nặng" vừa sắc vừa actionable.
2. **Blind spot lớn nhất: A.** Hào hứng nhưng bỏ qua việc không thể scale business high-margin trên một playbook pricing tự mâu thuẫn và SLA không staff nổi. Xây tầng hai trước khi có móng.
3. **Tất cả bỏ lỡ:** opportunity cost tổ chức. SRF đang giữa SRF 2.0 rebuild + scale ads + TPN. Dựng thêm một services org high-touch tranh giành cùng nguồn lực/sự tập trung hữu hạn. Không ai price cái focus dilution này.

### Reviewer 2
1. **Mạnh nhất: B.** Response duy nhất chỉ ra lỗi CỤ THỂ, kiểm chứng được: số không khớp ($63,315 published vs $25,500 thật), rule #3 mâu thuẫn ví dụ tuyến tính của chính nó. Đây là flaw factual, không phải opinion — và nó là root cause của đúng vấn đề tài liệu định ngăn.
2. **Blind spot lớn nhất: A.** Bỏ qua thực tế SLA-staffing và pricing chaos. "Nghĩ lớn hơn" vô nghĩa nếu nền móng sập.
3. **Tất cả bỏ lỡ:** liability pháp lý. Hứa 99.9% uptime + SLA credit cho broadcast client có air-date = exposure hợp đồng thật. Node fleet fail giữa render cho live broadcast, damages có thể vượt giá trị deal. Không ai nhắc liability cap.

### Reviewer 3
1. **Mạnh nhất: C.** Nối mọi critique trừu tượng vào một artifact sáng thứ Hai (quote calculator) và chỉ ra Director là bottleneck — điều sẽ giết SLA 24h. Practical và đúng.
2. **Blind spot lớn nhất: D.** Liệt kê rối loạn rất tốt nhưng dừng ở mô tả, không cho hướng chiến lược, và ngầm giả định strategy vào IaaS là đúng.
3. **Tất cả bỏ lỡ:** renewal Adcetera (cuối tháng 7) là phép thử LIVE của cả thesis. Nếu annual lock là sản phẩm thật, landing renewal đó là proof point quan trọng nhất — và nó đang diễn ra NGAY BÂY GIỜ. Không ai gọi nó là priority tức thời.

### Reviewer 4
1. **Mạnh nhất: E.** Phân tách whale vs commodity và đòi định nghĩa sản phẩm trước tactic là insight sâu nhất; nó định khung lại cả tài liệu.
2. **Blind spot lớn nhất: A.** Quá nhiều upside, không móng. Đúng về điểm đến (annual lock, LucidLink moat) nhưng sai về thứ tự — không thể marketing một certainty product khi chính SRF chưa định nghĩa được certainty đó hay reconcile nổi giá.
3. **Tất cả bỏ lỡ:** buyer vs user của cam kết năm. Tài liệu giả định người trong chat (Thomas King) là decision-maker. Trong studio, producer cảm nhận nỗi đau thường không kiểm soát budget năm. Yearly Lock pitch cần chạm budget owner — không ai address buying committee.

### Reviewer 5
1. **Mạnh nhất: B.** Catch số liệu là điểm quyết định — nó biến "tài liệu hơi lủng củng" thành "tài liệu không deploy được như hiện tại", có bằng chứng số học. Đây là thứ duy nhất nếu bỏ qua sẽ trực tiếp tái tạo Adcetera.
2. **Blind spot lớn nhất: B (chính nó).** Mạnh về flaw nhưng mỏng về con đường constructive — "fix trước khi bán" đúng nhưng thiếu "fix bằng cách nào". C và E lấp chỗ đó.
3. **Tất cả bỏ lỡ:** không response nào nối lại rằng quote calculator (C) chính là forcing function rẻ nhất để ÉP ra product definition (E) — bạn không thể build calculator mà không quyết bán gì, cho ai. Tactic và reframe thật ra là MỘT hành động.

---

## Kết Quả Vote
**Mạnh nhất:** B (Người Phản Biện) ×2 · E (Tư Duy Gốc) ×2 · C (Người Thực Thi) ×1
**Blind spot lớn nhất:** A (Người Mở Rộng) ×3 · D (Người Ngoài Cuộc) ×1 · B (Người Phản Biện) ×1

---

## Phán Quyết Chairman

### Council Đồng Thuận
Cả 5 đồng ý: tài liệu **well-intentioned, well-structured, nhưng CHƯA an toàn để vận hành**. Instinct của các procedure (paper trail, lock-after-payment, handoff, owning mistakes) đúng — chúng vá đúng lỗ hổng Adcetera.

4/5 hội tụ độc lập: **pricing reference là flaw chí mạng.** Người Phản Biện chứng minh bằng số (published $1,750/$1,172.50 → 18 machine × 3 tuần = $63,315 vs deal thật $25,500; rule #3 nói "non-linear" nhưng ví dụ tuyến tính hoàn hảo $8,500/tuần). Người Thực Thi xác nhận rep không ra nổi số defensible. Người Ngoài Cuộc không tái tạo nổi $25,500. Tư Duy Gốc chỉ ra product/price chưa được định nghĩa.

Hội tụ mạnh: Adcetera bị over-generalize (n=1, lại là near-miss). "Rough estimate + caveat" là band-aid, không phải fix cho root cause (không đưa được số defensible nhanh). Motion high-touch lệch với tier giá thấp — áp discovery call + Director approval + handoff cho giao dịch $300 là cost-to-serve lộn ngược (Tư Duy Gốc + Người Thực Thi + Người Ngoài Cuộc).

### Council Tranh Cãi
**Hai tranh cãi thật:**

1. **Người Mở Rộng (The Expansionist) vs Người Phản Biện + Tư Duy Gốc — upside vs móng.** Mở Rộng: nghĩ lớn — annual lock là sản phẩm thật, LucidLink là moat, đây là category play, rủi ro lớn nhất là nghĩ nhỏ. Phản Biện + Tư Duy Gốc: không xây tầng high-margin trên móng tự mâu thuẫn + SLA không staff nổi; và có lẽ không nên ở hai business cùng lúc. Cả hai đúng ở hai chân trời khác nhau. Giải: **móng trước** (fix pricing + SLA + segmentation), **rồi** category expansion.

2. **Tư Duy Gốc vs Người Thực Thi — reframe vs ship.** Gốc muốn lùi lại định nghĩa product/segmentation trước khi đụng tactic. Thực Thi nói intent đúng rồi, dựng quote calculator thứ Hai và iterate. Reviewer 5 hòa giải: **calculator chính là forcing function rẻ nhất để ÉP ra product definition** — không build được calculator mà chưa quyết bán gì cho ai. Tactic của Thực Thi PHỤC VỤ mục tiêu của Gốc. Không thật sự mâu thuẫn.

### Điểm Mù Council Phát Hiện
Qua peer review, 4 thứ cả 5 advisor đều bỏ:

1. **Opportunity cost tổ chức.** SRF đang giữa SRF 2.0 rebuild + scale ads $15–20K/tháng + TPN compliance. Dựng thêm một high-touch services org tranh cùng focus/capital hữu hạn. Có nên đứng full FSG org NGAY bây giờ, hay chạy IaaS cố ý nhỏ + founder-led tới khi SRF 2.0 ship?
2. **Liability pháp lý.** Hứa 99.9% uptime + SLA credit cho broadcast client có air-date cứng = exposure hợp đồng thật, không có liability cap nào trong tài liệu. Node fail giữa live broadcast render → damages có thể vượt giá trị deal.
3. **Renewal Adcetera (cuối tháng 7) là phép thử LIVE của cả thesis.** Nếu annual lock là sản phẩm thật, landing nó là proof point #1 — đang diễn ra ngay bây giờ, nhưng không advisor nào gọi là priority tức thời.
4. **Buyer vs user của cam kết năm.** Producer trong chat thường không kiểm soát budget năm; Yearly Lock cần chạm budget owner.

### Khuyến Nghị
Tài liệu là **bản nháp chiến lược tốt, nhưng KHÔNG phải operating manual deploy được**. KHÔNG roll out cho team như hiện tại — pricing tự mâu thuẫn sẽ chế tạo ra đúng cú sốc Adcetera nó định ngăn. Nhưng cũng đừng vứt — instinct đúng.

**Thứ tự đề xuất:**

1. **Fix móng trước khi deploy (1–2 tuần):**
   - (a) **Reconcile pricing** — dựng quote calculator (node type × count × duration → số defensible + caveat tự gắn) và giải quyết terminology node/machine/GPU + math Adcetera để bảng giá published, bảng duration, và deal thật khớp nhau.
   - (b) **Định nghĩa sản phẩm** — một "dedicated certainty" SKU với SLA + capacity guarantee viết rõ VÀ liability cap.
   - (c) **Segment motion** — self-serve/low-touch cho CPU commodity rental, full FSG white-glove chỉ trên ngưỡng deal-size (doc đã có sẵn qualifier $5k+).

2. **Rồi mới đánh play lớn (thesis Người Mở Rộng, nhưng SAU):** lead account cao cấp bằng Yearly Capacity Lock như sản phẩm chính (không phải upsell); coi LucidLink/Suite integration là moat; dùng case Adcetera (anonymized) làm external marketing cho segment broadcast.

3. **Để ý meta-risk:** cân nhắc kỹ SRF có đủ focus/capital đứng một services org high-touch TRONG LÚC rebuild SRF 2.0 không. Có thể chạy IaaS cố ý nhỏ + manual (whale-only, founder-led) tới khi SRF 2.0 ship, thay vì dựng full FSG org bây giờ.

**Lý do chairman nghiêng hướng này** (không theo số đông đơn thuần): reasoning kết hợp mạnh nhất = Tư Duy Gốc (định nghĩa product + segment) + Người Phản Biện (fix số) + Người Thực Thi (calculator là forcing function). Người Mở Rộng đúng về ĐIỂM ĐẾN nhưng sai về THỨ TỰ. Nên: móng trước, rồi mở rộng.

### Việc Đầu Tiên Cần Làm
**Dựng quote calculator một trang** biến (node type, count, duration) thành MỘT con số defensible với caveat estimate-vs-quote tự gắn — và trong lúc làm, ép giải quyết ba mâu thuẫn council tìm ra: (1) terminology node vs machine vs GPU; (2) bảng giá published $1,750/$1,172.50 ra con số Adcetera $25,500 thật bằng cách nào; (3) pricing theo duration là tuyến tính hay không. **Tới khi sheet đó tồn tại VÀ reconcile được, freeze rollout cho team** — vì pricing reference hiện tại sẽ tái tạo cú sốc Adcetera.

---
*Council gồm 5 lens: Người Phản Biện · Tư Duy Gốc · Người Mở Rộng · Người Ngoài Cuộc · Người Thực Thi. Karpathy LLM Council pattern.*
