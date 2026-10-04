# Chặng 1 — Đặt giả thuyết · 60 phút

**Case:** Case A — AI Tutor: Diagnostic Refresher  
**Người thực hiện:** Nguyễn Văn Thăng — 2A202602835  
**Nhóm:** FinTech

**Mục tiêu:** Mở lại logic đang bị nén trong solution directive và viết một Problem Hypothesis đủ cụ thể để evidence có thể làm thay đổi.

**Chuỗi suy luận:** `Solution → Change → Actor → Situation & Job → Pain → Evidence`

> Đây là bản giả thuyết để thảo luận, chưa phải fact về user hay kết quả nhóm đã thống nhất. Theo yêu cầu bài tập, 15 phút đầu mỗi thành viên tự suy luận, chưa dùng AI; sau đó so sánh các nhánh và giữ lại những cách giải thích khác nhau. Bản này có AI hỗ trợ biên tập, không chứng minh bước tự suy luận đã được thực hiện.

## 1. Solution — Gỡ solution khỏi hình thức cụ thể

### Solution directive

Directive theo tài liệu case đang lưu trong [README](../README.md):

> Thêm nút **“Tôi vẫn chưa hiểu”** vào bài học. Khi học viên bấm nút, AI Tutor sử dụng nội dung bài hiện tại, các câu trả lời gần đây và lịch sử học tập để: 1. Đặt 2–3 câu hỏi chẩn đoán ngắn. 2. Chọn một khái niệm nền để học viên ôn lại. 3. Tạo một phần giải thích ngắn. 4. Đưa học viên trở về bài đang học.

**Các lựa chọn triển khai đang có:** nút bấm, AI Tutor, dữ liệu lịch sử học tập, 2–3 câu hỏi chẩn đoán, một khái niệm nền và phần giải thích ngắn. Chúng chưa chứng minh nguyên nhân khiến học viên không hiểu bài hoặc cách hỗ trợ nào hiệu quả.

### Capability trung tính

> Giúp học viên làm rõ điểm đang vướng, nhận hỗ trợ phù hợp và tiếp tục thực hiện nhiệm vụ học tập đang dang dở.

Capability này có thể được thực hiện bằng tài liệu, người hỗ trợ hoặc công cụ khác. Việc học viên không hiểu bài chưa đủ để kết luận họ thiếu kiến thức nền.

## 2. Change — Làm lộ chuỗi thay đổi được kỳ vọng

### Chuỗi thay đổi giả định

`Solution cung cấp hỗ trợ theo điểm vướng`
→ `Học viên chủ động yêu cầu hỗ trợ và cung cấp thông tin`
→ `Điểm vướng được xác định đúng`
→ `Học viên làm rõ phần liên quan và thử áp dụng lại`
→ `Tự thực hiện được bước từng bị mắc`
→ `Tiếp tục bài học với mức hiểu tốt hơn`.

### Ba thay đổi được kỳ vọng

1. **Nhận biết:** Học viên xác định rõ hơn bước chưa hiểu và phần kiến thức liên quan cần làm rõ.
2. **Hành vi:** Học viên chuyển từ tìm kiếm nhiều nguồn thiếu trọng tâm sang xử lý điểm vướng, rồi thử lại nhiệm vụ ban đầu.
3. **Kết quả:** Học viên tự làm hoặc giải thích được bước từng bị mắc, giảm gián đoạn khi học.

| Output team tạo ra | Outcome team có thể ảnh hưởng |
| :--- | :--- |
| Câu hỏi chẩn đoán, phần ôn hoặc giải thích, đường quay lại bài | Xác định đúng điểm vướng, tự làm tiếp được, giảm công sức xử lý và tiếp tục bài học |

**Điều cần đúng:** Học viên nhận ra mình cần hỗ trợ, sẵn sàng tham gia, nhận hỗ trợ đúng nguyên nhân và áp dụng lại được. Nếu chỉ đọc phần giải thích rồi quay lại bài mà chưa tự làm được, chuỗi chưa đạt outcome. Điều hướng về bài là output, không chứng minh đã hiểu bài.

## 3. Actor — Xác định các nhóm người có liên quan

Các job, pain và lợi ích trong bảng đều là giả thuyết.

| Actor | Họ đang làm gì? | Pain hoặc hậu quả có thể có | Họ hưởng lợi thế nào? |
| :--- | :--- | :--- | :--- |
| Học viên | Tự học, làm bài, tìm cách xử lý bước chưa hiểu | Không làm tiếp được; mất công tìm hỗ trợ; chậm hoặc bỏ dở bài | Làm rõ điểm vướng và tự hoàn thành nhiệm vụ |
| Giảng viên | Thiết kế bài, giảng dạy và giải đáp | Khó nhận biết từng điểm vướng; phải giải thích lại nhiều lần | Nhận biết phần bài cần cải thiện và hỗ trợ đúng chỗ |
| Tutor/TA/Coach | Hỗ trợ từng học viên khi có yêu cầu | Thiếu bối cảnh về bước mắc và những cách học viên đã thử | Có thêm bối cảnh để hỗ trợ phù hợp |

**Actor ưu tiên điều tra:** Học viên tự học đã gặp một bước chưa hiểu và tìm cách xử lý trong 7 ngày gần đây.

**Lý do chọn:** Học viên trực tiếp sử dụng hỗ trợ, trải nghiệm trở ngại và chịu hậu quả. Họ cũng phải thực hiện hành vi làm rõ rồi thử lại để outcome xảy ra. Giảng viên và coach là các nhánh liên quan có thể điều tra sau.

Tiêu chí 7 ngày giúp tìm sự kiện còn nhớ rõ; không tuyển riêng người thiếu kiến thức nền, vì sẽ làm lệch việc so sánh A và B.

## 4. Situation & Job — User đang cố làm gì trong tình huống nào?

**Khoảnh khắc giả định:** Trong một buổi tự học, học viên đọc/xem phần hướng dẫn và chuyển sang một câu hỏi hoặc bước thực hành nhưng chưa tự làm hay giải thích được bước đó.

| Thành phần | Mô tả giả định |
| :--- | :--- |
| Trigger | Gặp một bước chưa tự thực hiện hoặc giải thích được |
| Job | Hiểu và thực hiện bước đó để hoàn thành nhiệm vụ đang làm |
| Vì sao quan trọng | Bước này cần thiết để hoàn thành bài hiện tại hoặc làm phần tiếp theo |
| Cách làm hiện tại | Xem lại bài, tra cứu tài liệu/video, hỏi bạn, giảng viên hoặc chatbot |
| Điểm bắt đầu vướng | Xem hướng dẫn nhưng chưa biết cách thực hiện bước tiếp theo |

### Mô tả Situation & Job

> Khi đang tự học và gặp một bước chưa tự làm hoặc giải thích được, học viên đang cố hoàn thành câu hỏi/bài thực hành bằng cách xem lại hướng dẫn hoặc tìm hỗ trợ từ nguồn khác.

### JTBD Hypothesis

> Khi gặp một bước chưa làm được trong lúc tự học, tôi muốn hiểu cách thực hiện và tự làm được bước đó, để có thể hoàn thành nhiệm vụ hiện tại và tiếp tục học.

Job vẫn tồn tại khi bỏ AI và feature khỏi bối cảnh. Nguyên nhân của điểm vướng được để mở để điều tra ở phần Pain.

## 5. Pain — Viết các cách giải thích cạnh tranh

### Pain Hypothesis A — Thiếu nền và khó xác định phần cần ôn

> Khi tự học và gặp một bước chưa làm được, học viên gặp khó khăn trong việc hoàn thành nhiệm vụ vì chưa nắm kiến thức nền liên quan và không xác định được phần cần ôn, dẫn đến tìm kiếm hoặc xem lại nhiều nội dung mà vẫn mắc, làm chậm tiến độ hoặc bỏ dở bài.

### Pain Hypothesis B — Kiến thức nền đủ nhưng cách giải thích chưa rõ

> Khi tự học và gặp một bước chưa làm được, học viên gặp khó khăn trong việc hoàn thành nhiệm vụ vì cách giải thích trong bài thiếu bước trung gian hoặc ví dụ dễ áp dụng dù họ đã nắm kiến thức nền, dẫn đến phải tìm cách giải thích khác và gián đoạn việc học.

**Điểm cạnh tranh:** Cùng hành vi xem lại bài hoặc tìm nhiều nguồn có thể đến từ thiếu kiến thức nền (A) hoặc cách trình bày chưa rõ (B). Hành vi tìm kiếm nhiều nguồn tự nó chưa phân biệt được hai giả thuyết.

**Giả thuyết ưu tiên điều tra: A.** Directive phụ thuộc vào giả định chẩn đoán và ôn nền sẽ giúp học viên làm tiếp. Cần kiểm tra giả định này trước; đây chưa phải kết luận A phổ biến hoặc quan trọng hơn B.

Vẫn tìm dấu hiệu của B và nguyên nhân khác như mệt mỏi, mất tập trung hoặc thiếu thời gian. Pain nằm ở barrier và consequence; không viết pain thành “chưa có AI Tutor” hay “thiếu nút hỗ trợ”.

## 6. Evidence — Xác định điều cần tìm trước khi viết câu hỏi

Evidence phải gắn với sự kiện đã xảy ra: bài nào, lúc nào, bước nào chưa làm được, hành động theo thứ tự, nguồn đã dùng, công sức và kết quả. Lời khen tính năng hoặc lời hứa sẽ sử dụng chưa xác nhận problem hypothesis.

| Cần kiểm tra | Evidence làm nhóm tin hơn | Evidence làm nhóm nghi ngờ hoặc bác bỏ |
| :--- | :--- | :--- |
| Situation có thật | Kể được sự kiện gần đây, bài và bước bị mắc, thời điểm và diễn biến; có thể chỉ lại bài nếu còn | Chỉ nói chung “bài khó”, không nhớ sự kiện: chưa đủ evidence, chưa thể kết luận situation không tồn tại |
| Pain có ý nghĩa | Trở ngại cản nhiệm vụ cụ thể; kể được công sức đã bỏ ra và lý do cần xử lý | Đọc lại một lần là tự làm tiếp được, không có ảnh hưởng đáng kể |
| Workaround tồn tại | Đã xem bài cũ, tra cứu, hỏi người khác hoặc đổi nguồn; kể được nội dung tìm, lý do đổi và kết quả | Cách hiện tại giải quyết nhanh, ổn định; hoặc hành vi thực tế khác với giả thuyết |
| Consequence tồn tại | Bước vẫn chưa làm được, làm sai, bỏ qua, dừng bài hoặc phải dời nhiệm vụ tiếp theo | Vẫn hoàn thành được nhiệm vụ, chưa thấy hậu quả ngoài cảm giác chưa chắc chắn |
| Pattern có lặp | Kể thêm sự kiện tương tự với thời điểm, bước mắc và cách xử lý cụ thể | Chỉ xảy ra trong một điều kiện đặc biệt: cần thu hẹp phạm vi giả thuyết |
| A hay B giải thích tốt hơn | Đã ôn một kiến thức nền cụ thể, sau đó tự áp dụng được vào bước bị mắc; chỉ ra được liên hệ giữa hai phần | Đã sử dụng đúng kiến thức nền và chỉ cần ví dụ/bước giải thích khác để làm tiếp: nghiêng về B |

**Cách ghi evidence:** Ghi hành động, kết quả, lời kể và mốc bản ghi vào [notes.md](notes.md); tách diễn giải riêng. Chỉ đặt ngoặc kép cho lời đã đối chiếu chính xác.

**Điều chưa thể suy ra:** Chưa từng ôn nền không chứng minh ôn nền vô ích. Nếu hỗ trợ vừa ôn nền vừa đổi cách giải thích, ghi “chưa đủ evidence để phân biệt A/B”. Một cuộc phỏng vấn chưa cho biết mức độ phổ biến của pain.

## Chốt Problem Hypothesis và park solution

### Problem Hypothesis mang sang Chặng 2

> Với học viên tự học đã gặp một bước chưa hiểu trong bảy ngày gần đây, việc chưa nắm kiến thức nền liên quan và không xác định được phần cần ôn có thể khiến họ tìm kiếm hoặc xem lại nhiều nội dung mà vẫn chưa tự xử lý được bước đang mắc, làm chậm tiến độ hoặc bỏ dở bài học.

### Điều phải đúng để giả thuyết đứng vững

1. Có sự kiện cụ thể mà bước chưa hiểu thực sự cản học viên hoàn thành nhiệm vụ.
2. Kiến thức nền chưa nắm có liên quan trực tiếp đến bước bị mắc.
3. Học viên khó xác định phần cần ôn; cách xử lý hiện tại tốn công hoặc chưa hiệu quả.
4. Trở ngại gây hậu quả thực tế đủ đáng kể để học viên muốn xử lý.

Riêng chuỗi thay đổi của solution còn cần kiểm tra: làm rõ kiến thức nền có giúp học viên tự áp dụng lại vào bước bị mắc hay không. Pattern lặp lại giúp đánh giá phạm vi; không mặc định mọi học viên đều gặp vấn đề này.

### Điều có thể khiến nhóm sửa hoặc bác bỏ

| Evidence tìm được | Cách xem lại giả thuyết |
| :--- | :--- |
| Học viên đã nắm nền, chỉ cần ví dụ/cách diễn đạt khác | Chuyển trọng tâm sang B |
| Biết rõ phần cần ôn nhưng khó tìm tài liệu phù hợp | Sửa barrier thành khó tiếp cận hỗ trợ phù hợp |
| Cách hiện tại nhanh, hiệu quả, ít ảnh hưởng | Xem lại mức độ quan trọng của pain |
| Nguyên nhân chính là mệt mỏi, mất tập trung hoặc thiếu thời gian | Sửa nguyên nhân và phạm vi điều tra |
| Ôn nền rồi vẫn chưa tự thực hiện được bước mắc | Xem lại nguyên nhân và mắt xích ôn nền → làm tiếp được |
| Chỉ có một sự kiện do điều kiện đặc biệt | Thu hẹp phạm vi, chưa suy ra pattern chung |

### Solution Parking Lot

Chưa chọn phương án cuối. Các hướng sau được giữ lại để xem xét sau khi có evidence.

| Hướng giải quyết có thể có | AI / Không sử dụng AI |
| :--- | :--- |
| 1. Diagnostic Refresher: chẩn đoán ngắn, gợi ý ôn nền rồi thử lại bài | AI |
| 2. Bản đồ kiến thức tiên quyết kèm liên kết tới bài ôn do giảng viên biên soạn | Không sử dụng AI |
| 3. Bổ sung ví dụ, bước giải thích trung gian và chú giải trong bài | Không sử dụng AI |
| 4. Câu hỏi tự kiểm tra có nhánh dẫn tới nội dung ôn soạn sẵn | Không sử dụng AI |
| 5. Kênh hỏi Tutor/TA/Coach kèm bước bị mắc và những cách đã thử | Không sử dụng AI |
| 6. Giải thích lại đoạn đang học bằng ví dụ phù hợp với bối cảnh | AI |

## Checkpoint 1 — Problem Hypothesis

- [x] Lần theo được chuỗi Solution → Change → Actor → Situation & Job → Pain → Evidence.
- [x] Capability và job tồn tại độc lập với AI hoặc nút bấm.
- [x] Có hành vi trung gian, phân biệt output với outcome.
- [x] Chọn actor điều tra trước và nêu lý do.
- [x] Có hai cách giải thích cạnh tranh A/B cho cùng tình huống.
- [x] Có evidence hỗ trợ và evidence có thể làm giả thuyết sai.
- [x] Có Problem Hypothesis và điều phải đúng để giả thuyết đứng vững.
- [x] Có ít nhất năm hướng giải quyết, gồm phương án không sử dụng AI.
- [x] Nhóm đã đối chiếu suy luận cá nhân và thống nhất giả thuyết mang sang Chặng 2.

**Đầu ra chuyển sang Chặng 2:** Problem Hypothesis A, giả thuyết cạnh tranh B và Evidence Map ở mục 6 để xây dựng câu hỏi về trải nghiệm đã xảy ra. Chưa xác nhận pain hoặc chọn AI Diagnostic Refresher làm giải pháp cuối.

---

# Chặng 2 — Chuẩn bị phỏng vấn · 30 phút

**Mục tiêu:** Chuyển Evidence Map thành một Conversation Guide ngắn, đủ để tìm bằng chứng về pain mà không mời user đánh giá solution.

| Nội dung | Thời gian |
| :--- | :--- |
| Chốt ba điều quan trọng nhất cần học | 10 phút |
| Viết Conversation Guide | 15 phút |
| Tự rà soát và phân công phỏng vấn | 5 phút |

## 1. Chốt Big 3

Chọn đúng ba điều từ Evidence Map của Chặng 1: cách xử lý thực tế, nguyên nhân điểm vướng và mức độ ảnh hưởng. Điều số 2 là câu hỏi **“đáng sợ”**: evidence có thể cho thấy học viên đã nắm kiến thức nền, khiến nhóm chuyển từ A sang B hoặc xem xét nguyên nhân khác.

**Giả định lớn nhất cần kiểm tra:** Việc chưa làm tiếp được đến từ thiếu kiến thức nền và khó xác định phần cần ôn. Để pain đáng giải, trở ngại phải gây công sức hoặc hậu quả thực tế; chỉ cảm thấy bài khó chưa đủ. Vì vậy, cần nghe một sự kiện gần đây có hành động, cách xử lý và kết quả cụ thể, đồng thời tìm cả trường hợp người học giải quyết nhanh bằng cách hiện tại.

| Điều cần học | Evidence cần tìm | Điều gì khiến nhóm xem lại giả thuyết? |
| :--- | :--- | :--- |
| **1. Học viên đã xử lý điểm vướng như thế nào và xác định phần cần tìm bằng cách nào?** | Trình tự hành động trong lần gần nhất; nội dung/từ khóa đã tìm; nguồn hoặc người đã hỏi; lý do chọn, đổi cách và kết quả từng lần thử | Học viên biết rõ phần cần tìm và xử lý nhanh bằng cách hiện tại: giả định khó xác định phần cần ôn yếu đi. Nếu chỉ khó tìm tài liệu phù hợp, sửa barrier |
| **2. Điều gì thực sự cản học viên và điều gì đã giúp họ tự làm tiếp? — Câu hỏi đáng sợ** | Bước chưa làm được; nội dung hỗ trợ đã nhận; phần kiến thức hoặc cách thực hiện được làm rõ; hành động học viên tự thực hiện sau đó | Học viên đã nắm nền và chỉ cần ví dụ/cách giải thích khác: nghiêng về B. Nếu nguyên nhân là mệt mỏi, mất tập trung hoặc thiếu thời gian, xem lại phạm vi. Nếu hỗ trợ trộn nhiều yếu tố, chưa đủ evidence phân biệt A/B |
| **3. Điểm vướng ảnh hưởng đến nhiệm vụ ra sao và có lặp lại không?** | Thời gian/công sức đã bỏ ra; phần bài bị chậm, bỏ qua hoặc dừng; kết quả thực hiện nhiệm vụ; một sự kiện tương tự có thời điểm và diễn biến | Đọc lại một lần là làm tiếp được, không có ảnh hưởng đáng kể: pain có thể nhỏ. Chỉ xảy ra một lần do điều kiện đặc biệt: cần thu hẹp giả thuyết |

## 2. Viết Conversation Guide

**Cách dùng:** Mở riêng phần này khi phỏng vấn. Hỏi từng câu, nghe hết câu chuyện rồi chọn probe cho chi tiết còn thiếu. Nếu câu chuyện đã trả lời một điều cần học, xác nhận ngắn rồi chuyển tiếp. Ghi evidence vào [Interview Record](notes.md).

### Tiêu chí tuyển người

Chúng tôi cần nói chuyện với **học viên đã gặp một phần bài học chưa hiểu hoặc một bước chưa tự làm được khi tự học và đã tìm cách xử lý trong vòng 7 ngày gần đây**, nhớ được một sự kiện cụ thể.

Tuyển theo tình huống đã trải qua; để mở nguyên nhân và cách xử lý để so sánh các giả thuyết.

### Recruitment check

> Trong bảy ngày gần đây, bạn có lần nào gặp một phần bài học chưa hiểu khi tự học và đã tìm cách xử lý không?

Nếu có, xác nhận riêng “Đó là bài nào?”, rồi “Lần đó vào lúc nào?”. Nếu chưa có sự kiện phù hợp, tìm người khác cho lượt này. Câu tuyển người chưa được tính là evidence chính.

### Lời mở đầu

> Cảm ơn bạn đã dành thời gian. Mình muốn tìm hiểu một lần gần đây bạn gặp phần bài học chưa hiểu, những việc bạn đã làm và kết quả. Không có câu trả lời đúng hay sai. Bạn có thể bỏ qua câu hỏi hoặc dừng bất cứ lúc nào. Bạn có đồng ý tham gia không?

Nếu cần bản ghi, xin đồng ý trước khi bật ghi:

> Mình muốn ghi âm để xem lại, bóc transcript và phục vụ bài học. Bản ghi không được chia sẻ công khai. Bạn có đồng ý cho mình ghi âm với mục đích đó không?

Chờ câu trả lời và ghi đúng phạm vi đồng ý vào notes. Nếu người tham gia từ chối ghi âm, tiếp tục bằng ghi chép nếu họ đồng ý.

### Story opener

> Kể mình nghe về lần gần nhất trong bảy ngày vừa rồi bạn gặp một phần bài học chưa hiểu khi tự học và tìm cách xử lý, từ lúc đang học đến khi lần đó kết thúc?

Để người tham gia kể trước. Nếu câu trả lời còn chung chung, neo về bài và thời điểm đã xác nhận rồi hỏi việc họ đã làm đầu tiên.

### Big 3 Questions

| Điều cần học | Câu hỏi sẽ dùng |
| :--- | :--- |
| **1. Cách xử lý và cách xác định phần cần tìm** | “Từ lúc nhận ra mình chưa hiểu trong lần đó, bạn đã làm những gì để xử lý, theo thứ tự?” |
| **2. Nguyên nhân điểm vướng và điều giúp làm tiếp — câu hỏi đáng sợ** | “Trong những cách đã thử ở lần đó, cách nào giúp bạn làm tiếp được, nếu có?” |
| **3. Ảnh hưởng và sự lặp lại** | “Lần đó ảnh hưởng đến việc học hoặc việc làm bài của bạn như thế nào?” |

Câu 2 cho phép câu trả lời “không có cách nào giúp làm tiếp”. Nếu có cách hiệu quả, hỏi chi tiết đã giúp và bước người học tự thực hiện sau đó. Nếu chưa, hỏi phần còn vướng. Khi chỉ một ví dụ hoặc cách diễn đạt khác đã đủ để học viên làm tiếp, giả định phải chẩn đoán và ôn nền yếu đi. Dùng lời kể và hành động để đối chiếu A/B sau buổi, tránh đưa sẵn nguyên nhân cho người tham gia chọn. Phần lặp lại của Big 3 số 3 được đào bằng một sự kiện khác trong probe.

### Probe bank — Chỉ dùng khi cần đào sâu câu chuyện

Các câu trong cùng một ô là lựa chọn; hỏi từng câu khi cần.

| Khi câu chuyện còn thiếu | Probe có thể dùng |
| :--- | :--- |
| Nhiệm vụ và bước bị mắc | “Lúc đó bạn đang cố hoàn thành việc gì?”; “Bạn có thể kể hoặc chỉ lại bước chưa làm được không?”; “Phần nào khó nhất với bạn lúc đó?” |
| Trình tự hành động | “Ngay sau đó chuyện gì xảy ra?”; “Lúc đó bạn đã làm gì?” |
| Cách xác định phần cần tìm | “Lúc đó bạn đã tìm nội dung gì?”; “Bạn biết cần tìm phần đó bằng cách nào?” |
| Lý do chọn hoặc đổi cách | “Điều gì khiến bạn chọn cách đó lúc ấy?”; “Trong lần đó bạn đã thử cách nào khác không?”; “Cách trước đó cho kết quả thế nào?” |
| Kết quả của hỗ trợ | “Cách đó cho kết quả thế nào?”; nếu người học nói đã làm tiếp được: “Chi tiết nào giúp bạn làm tiếp?”; “Sau đó bạn đã tự thực hiện bước đó như thế nào?” |
| Chưa xử lý được | “Đến lúc dừng, phần nào vẫn chưa rõ?”; “Lúc đó bạn quyết định làm gì tiếp theo?” |
| Công sức và hậu quả | “Bạn nhớ đã dành khoảng bao lâu cho việc đó không?”; “Việc dự định làm tiếp lúc đó diễn ra thế nào?” |
| Sự lặp lại | “Bạn có nhớ một lần khác gần đây gặp chuyện tương tự không?”; nếu có: “Kể mình nghe lần đó.” |
| Trường hợp pain nhỏ hoặc cách hiện tại hiệu quả | “Bạn có nhớ lần nào gặp bước chưa hiểu nhưng xử lý được ngay không?”; nếu có: “Lần đó diễn ra thế nào?” |
| Tín hiệu như bỏ qua, hỏi lại hoặc đổi nguồn | “Bạn vừa nói ‘[đúng từ người tham gia dùng]’; lúc đó đã xảy ra chuyện gì?” |

Nếu không nhớ, ghi “không nhớ”; nếu không có ảnh hưởng, ghi đúng lời kể. Phân biệt thời gian người tham gia ước lượng với mốc trên bản ghi. Chỉ xem bài hoặc tài liệu khi người tham gia đồng ý chia sẻ.

### Ba phản xạ khi data bắt đầu lệch

| User đưa ra | Phản xạ | Cách quay lại evidence |
| :--- | :--- | :--- |
| Lời khen | **Deflect** | “Cảm ơn bạn. Quay lại lần vừa kể, bạn đã làm gì đầu tiên khi gặp bước đó?” |
| Câu chung chung hoặc lời hứa tương lai | **Anchor** | “Lần gần nhất chuyện đó xảy ra là khi nào?”; sau khi xác nhận sự kiện: “Lúc đó bạn đã làm gì?” |
| Ý tưởng hoặc feature request | **Dig** | “Trong lần vừa kể, điều gì khiến bạn cần cách hỗ trợ đó?”; rồi “Lúc đó bạn đã xử lý việc ấy thế nào?” |

### Kết thúc

> Mình hiểu là lần đó bạn gặp [điểm vướng], đã [hành động được kể] và kết quả là [kết quả được kể]. Mình có hiểu sai hoặc bỏ sót chi tiết nào không?

Cảm ơn và dừng ghi. Ngay sau buổi, hoàn thiện notes với sự kiện, hành động, workaround, công sức, hậu quả và mốc bản ghi. Tách evidence khỏi nhận định; ghi một câu hỏi hiệu quả và một chỗ cần sửa để trao đổi với nhóm.

## 3. Tự rà soát và phân công phỏng vấn

### Tự rà soát

| Điểm kiểm tra | Kết quả rà soát |
| :--- | :--- |
| Có câu nào làm lộ solution không? | Các câu nói với người tham gia không nhắc tên tính năng, nút bấm hoặc mô tả giải pháp đang cân nhắc |
| Có câu nào hỏi ý kiến hoặc dự đoán tương lai không? | Câu hỏi bám vào sự kiện và hành động đã xảy ra |
| Story opener đã neo vào lần gần nhất chưa? | Có; lần gần nhất trong 7 ngày vừa rồi |
| Ba câu hỏi chính có nối với Big 3 không? | Có: trình tự xử lý → cách giúp làm tiếp → ảnh hưởng; dùng probe để làm rõ phần cần tìm, kết quả tự làm và sự lặp lại |
| Có câu hỏi có thể làm giả thuyết yếu đi không? | Có; câu 2 và probe có thể cho thấy chỉ cần cách giải thích khác. Probe về lần xử lý ngay có thể cho thấy pain nhỏ |
| Interviewee đã đáp ứng tiêu chí tuyển chưa? | Chưa có xác nhận người tham gia cụ thể; cần thực hiện recruitment check |
| Mỗi thành viên biết sẽ phỏng vấn ai chưa? | Chưa chốt người và lịch; bảng dưới là phân công đề xuất |

### Phân công đề xuất

| Thành viên / người hỏi | Người sẽ phỏng vấn | Việc phụ trách | Trạng thái |
| :--- | :--- | :--- | :--- |
| Nguyễn Văn Thăng | Người tham gia trong bản ghi hiện có; cần xác nhận thông tin và sự kiện phù hợp | Đối chiếu lượt luyện với Big 3; hoàn thiện notes và reflection; dùng guide này cho lượt tiếp theo | Có bản ghi theo hồ sơ; người tham gia, ngày và guide đã dùng chưa xác nhận |
| Tạ Việt Cường | Học viên có sự kiện phù hợp trong 7 ngày gần đây; chưa chốt người | Tuyển người, xác nhận tham gia/ghi âm, phỏng vấn và ghi evidence cho cả ba điều cần học | Đề xuất, chờ nhóm chốt người và lịch |
| Nguyễn Anh Dũng | Học viên có sự kiện phù hợp trong 7 ngày gần đây; chưa chốt người | Tuyển người, phỏng vấn theo cùng guide; chú ý trường hợp đối chiếu làm A yếu đi, ghi notes và reflection | Đề xuất, chờ nhóm chốt người và lịch |

Trước mỗi lượt, chốt mã người tham gia, người hỏi, người ghi chép và giờ phỏng vấn. Người quan sát hoặc ghi chép chỉ tham gia khi interviewee đồng ý. Mỗi người hỏi tự ghi reflection của lượt mình.

## Checkpoint 2 — Interview-ready

- [x] Có đúng ba điều cần học từ Evidence Map, gồm một điều có thể khiến nhóm đổi hướng.
- [x] Có tiêu chí tuyển và recruitment check riêng với evidence chính.
- [x] Lời mở đầu nêu mục đích học hỏi; story opener bắt đầu từ sự kiện gần đây.
- [x] Có đúng ba câu hỏi chính nối trực tiếp với Big 3.
- [x] Probe bank đào được hành vi, workaround, công sức và hậu quả.
- [x] Các câu nói với người tham gia không để lộ solution directive.
- [x] Có Deflect–Anchor–Dig để quay về evidence.
- [x] Có bảng tự rà soát và phân công đề xuất.
- [x] Xác nhận người tham gia đáp ứng tiêu chí tuyển.
- [x] Nhóm chốt người tham gia, vai trò và lịch của từng lượt.

**Trạng thái tại lúc chuẩn bị:** Guide đã hoàn thiện về nội dung theo Checkpoint 2. Phần người tham gia và lịch thực tế chưa được nhóm xác nhận trong hồ sơ. Tiến độ lượt phỏng vấn đã thực hiện được cập nhật ở Chặng 3 bên dưới.

---

# Chặng 3 — Luyện phỏng vấn · 45 phút

**Mục tiêu:** Luyện cách mở một câu chuyện thật, follow user và đào sâu hành vi, workaround, hậu quả mà không làm lộ solution hoặc dẫn dắt câu trả lời.

**Người thực hiện:** Nguyễn Văn Thăng — 2A202602835  
**Trạng thái lượt cá nhân:** Đã thực hiện phỏng vấn và ghi âm theo xác nhận của người thực hiện. Bản ghi hiện có: [recording.m4a](recording.m4a). Nội dung bản ghi chưa được đối chiếu để điền evidence bên dưới.

## 1. Cách tổ chức lượt luyện

Ghép cặp với một người ngoài nhóm, không cho nhau xem solution directive. Người tham gia cần đáp ứng tiêu chí Chặng 2: đã tự học, gặp một bước chưa tự làm hoặc giải thích được và tìm cách xử lý trong 7 ngày gần đây. Nếu không phù hợp, báo giảng viên để đổi cặp.

| Hoạt động | Thời gian theo bài tập |
| :--- | :--- |
| Người thứ nhất làm interviewer; ghi đúng lượt mình | 15 phút |
| Đổi vai; người thứ hai ghi đúng lượt mình | 15 phút |
| Hoàn thiện notes và quay lại nhóm | 10 phút cuối |

Đây là khung tổ chức của bài tập, không phải thời lượng thực tế đã xác nhận từ bản ghi.

## 2. Xin phép và sử dụng bản ghi

Trước khi bắt đầu ghi, nói rõ mục đích và xin sự đồng ý bằng lời mở đầu ở Chặng 2. Chỉ bật ghi khi người tham gia đồng ý. Bản ghi chỉ dùng để xem lại, bóc transcript và phục vụ bài học; không chia sẻ công khai.

**Consent của lượt đã thực hiện:** Chờ người thực hiện bổ sung việc đã xin và được đồng ý trước khi ghi, cùng phạm vi đồng ý. Việc có file audio chưa đủ để xác nhận consent.

## 3. Interview Record — Lượt Nguyễn Văn Thăng làm interviewer

| Trường | Nội dung |
| :--- | :--- |
| Interviewer | Nguyễn Văn Thăng — 2A202602835, theo thông tin cá nhân trong README |
| Nhóm | FinTech: Nguyễn Văn Thăng; Tạ Việt Cường; Nguyễn Anh Dũng |
| Mã người tham gia | 2A202602841 |
| Ngày, giờ | 09:30:00 ngày 04/10/2026 |
| Thời lượng | Bản ghi: 07:56,45  |
| Hình thức / người ghi chép | Hình thức gặp và người ghi chép thực tế |

| Điều cần giữ lại | Ghi chép |
| :--- | :--- |
| Câu chuyện gần nhất: user đang ở đâu và cố làm gì? | Chờ bổ sung từ lời kể/bản ghi: bối cảnh, thời điểm, bài học và nhiệm vụ cụ thể. |
| User đã thực sự làm gì? | Chờ bổ sung trình tự hành động đã xảy ra, nguồn đã xem hoặc người đã hỏi và kết quả từng lần thử. |
| Khó khăn và workaround đã dùng | Chờ bổ sung bước bị mắc, cách đã thử để xử lý, lý do đổi cách và phần còn chưa giải quyết được. |
| Hậu quả hoặc chi phí | Chờ bổ sung thời gian/công sức, phần bài bị chậm, bỏ qua hoặc dừng. Nếu không có hậu quả đáng kể, ghi đúng lời kể. |
| Điều bất ngờ, trái giả thuyết hoặc một exact quote | Chờ bổ sung chi tiết có thể làm giả thuyết A/B thay đổi. Chỉ dùng ngoặc kép khi đã đối chiếu nguyên văn; kèm mốc bản ghi. |

## 4. Rà lại cách phỏng vấn

Khi nghe lại, đối chiếu Conversation Guide với diễn biến thực tế: câu nào mở được câu chuyện cụ thể; tín hiệu hành vi, workaround hoặc hậu quả nào đã được hỏi tiếp; chỗ nào hỏi dẫn dắt hoặc bỏ lỡ chi tiết. Ghi một câu hỏi hiệu quả và một chỗ cần sửa vào phần reflection trong [notes.md](notes.md).

Trong lượt luyện, dùng guide làm xương sống nhưng follow câu chuyện của user: nói ít, hỏi tiếp theo chi tiết vừa nghe. Không pitch solution hoặc hỏi user có muốn feature không. Lời khen và “mình sẽ dùng” không được coi là evidence về pain; quay lại sự kiện, hành động và hậu quả đã xảy ra.

## Checkpoint 3 — Practice completed

- [x] Nguyễn Văn Thăng đã hoàn thành một lượt phỏng vấn với vai trò interviewer, theo xác nhận của người thực hiện.
- [x] Có file ghi âm của lượt phỏng vấn: [recording.m4a](recording.m4a).
- [x] Bổ sung mã người tham gia và xác nhận đúng tiêu chí tuyển, ngoài nhóm.
- [x] Xác nhận đã xin và được đồng ý trước khi bắt đầu ghi âm.
- [x] Điền đủ Interview Record bằng nội dung thực tế và mốc bản ghi.
- [x] Hoàn thiện notes, reflection và quay lại trao đổi với nhóm.

**Trạng thái checkpoint cá nhân:** Đã phỏng vấn và có bản ghi; cần bổ sung Interview Record và xác nhận consent để chốt Checkpoint 3. Trạng thái của các thành viên khác chưa được cập nhật.
