---
title: "Game Designer Là Mắt Xích Cỗ Máy"
source: "[[raw/videos/negaxy-iec-gd-doc-01-gd-role-mindset]]"
date_added: 2026-05-15
tags: [concept, game-design, mindset, role, define]
aliases: [vai trò game designer, GD là mắt xích, define cho code và art]
status: draft
related:
  - "[[5-levels-of-idea]]"
  - "[[ltv-cpi-formula]]"
  - "[[file-y-do-design-intent]]"
  - "[[prototype-vs-mvp]]"
summary: "GD không phải vị trí ra lệnh — là một mắt xích trong cỗ máy sản xuất, có trách nhiệm define đủ thông tin cho code và art làm việc được"
---

## Định Nghĩa

Vũ (lecturer khóa Negaxy + IEC) định nghĩa game designer là **một mắt xích trong cỗ máy sản xuất game**, không phải vị trí ra lệnh. Quote nguyên văn: *"Các bạn nói cái gì thì cốt phải làm cho. Các bạn nói cái gì là phải làm thế nào với đấy. Thực ra thì góc nhìn của mình hơi khác. Mình nghĩ cái design nó là một mắt xích trong cả một cỗ máy."*

Vai trò "đúng" của GD là define đủ thông tin để các mắt xích khác (code, art, marketing) làm việc được. Nếu code không làm nổi hoặc art kêu deadline không đủ, Vũ đặt câu hỏi: *"vậy các bạn đã hoàn thành vai trò của mình hay chưa?"*

## Define Cho Code

Code làm việc bằng *"đúng sai, là luồng, là hàm, là logic"* — designer không thể mô tả lượn văn rồi mong code đoán ý. Mỗi function phải có input/output rõ ràng trước khi build.

Ví dụ Vũ đưa ra cho game 2 nhân vật (skill lửa + skill băng): khi 2 effect đè lên một mục tiêu, kết quả là gì? Băng đông cứng nhưng bị rã đông? Cả hai cancel nhau? Sinh ra một effect mới (steam)? *"Đó là quyền của các bạn — nhưng bạn phải define được cái đầu ra."*

Cho game vật lý (case RedBone của Đạt): GD cần define **trước** các tham số (kích thước, khối lượng, chất liệu cho ma sát, đồ thị gia tốc khi nhấn nút, mức plateau, hành vi khi nhả tay), **sau đó** mới đến phần tuning bằng cảm giác. Đạt thừa nhận team không define rõ ngay từ đầu, chủ yếu "cảm giác và điều chỉnh lại" — Vũ đánh giá là anti-pattern.

Nguyên tắc tổng kết: *"Hãy giảm bớt thời gian từ cái đoạn làm đúng, để tăng cái đoạn làm hay lên."* Vũ chia dự án thành 2 đoạn — làm đúng (function works) và làm hay (polish). Define tốt thì đoạn 1 ngắn, có chỗ cho đoạn 2.

## Define Cho Art

Vấn đề điển hình: *"Các bạn art sẽ có xu hướng vẽ từng chi tiết đẹp, thay vì đưa ra một tầm bố cục đẹp."* Art không biết hết ràng buộc kỹ thuật hay timeline dự án — GD phải đưa ra giới hạn để art sáng tạo trong khung.

Ví dụ Tower Defense 3D: thiết bị tham chiếu xử lý max ~100k triangles, 80 mob cùng màn → mỗi mob chỉ được ~3k tris. Nếu art vẽ con boss 15k tris vì "đẹp" thì vỡ trận. GD phải đưa tham số trước. Xem [[asset-hardware-tradeoff]] cho deep-dive về trade-off này.

Color clash là một dạng define khác: red bomb đỏ, một effect biến nó thành golden → bỗng cùng màu vàng với toàn bộ quân đồng minh, lẫn vào nhau. GD phải nghĩ trước những combo color như vậy.

## Dataflow Diagram — Output Cuối Của GD

Khi làm với studio Trung Quốc, Vũ mô tả cycle define đầy đủ: **doc → break down → flow chart → dataflow diagram**. Đến dataflow, *"cốt gần như là đoạn đọc phía trên chỉ để hiểu cái này làm cái gì thôi — đa phần nó xem dataflow chạy dữ liệu từ đâu sang, mỗi chức năng nó nhận cái gì, trả cái gì, trả về chỗ nào."*

Lập luận: người **nghĩ ra** function là người hiểu sâu nhất. Bộ phận khác có thể làm dataflow, nhưng không thể tốt bằng người tạo ra concept. Đây là lý do Vũ không chấp nhận argument *"em chỉ thuần làm GD, em chỉ mô tả công năng thôi"* — GD phải đi tới mức dataflow cho function của mình.

## Liên Hệ Wiki

Khung "GD là mắt xích" là tiền đề cho [[5-levels-of-idea]] (5 mức độ chín của idea khi thuyết phục sếp — level 3 đòi GD biết cách triển khai chứ không chỉ list element). [[file-y-do-design-intent]] là tài liệu cụ thể GD viết để truyền define từ ý đồ xuống output. Trong [[prototype-vs-mvp]], prototype là base để team đập vào comment chứ không phải bản hoàn thiện — phản ánh đúng tinh thần "define đủ để chạy tiếp" thay vì "tự hoàn thiện hết một mình".

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-01-gd-role-mindset.md` § "Vai Trò Của Game Designer", "Define Cho Code", "Define Cho Art", "GD Phải Cover Cái Gì"
