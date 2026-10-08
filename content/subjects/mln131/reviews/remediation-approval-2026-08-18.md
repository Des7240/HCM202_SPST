# Audit, remediation và phê duyệt lại MLN131 — 2026-08-18

## Phạm vi khóa

- Nguồn duy nhất: `giao-trinh-chu-nghia-xa-hoi-khoa-hoc-2021.md`.
- SHA-256 nguồn: `1379d246e3466b5451752e31279c50081b85894296c3feea873fa68fd66c6ee8`.
- Phạm vi review: 7/7 chương, 280/280 câu, 1.120/1.120 phương án và 56/56 câu Vận dụng.
- Canonical bank cuối: `c0d05afb13a708fc7a95c63d92882ad809931b10eff6ad5683d9fc0cc4fbde39`.

Phê duyệt ngày 2026-08-03 đã mất hiệu lực ngay khi ngân hàng được sửa. Đợt này review và ký lại trên đúng hash nêu trên.

## Findings đã xử lý

| Mức | Nhóm finding đã đóng | Open |
|---|---:|---:|
| Critical | 1 | 0 |
| High | 18 | 0 |
| Medium | 12 | 0 |
| Low | 1 | 0 |

Các nhóm chính gồm: toàn bộ phương án bị nhiễm câu đệm máy móc; câu Vận dụng chỉ đổi nhãn nhưng không có tình huống; dấu hiệu đoán đáp án theo độ dài; khóa đáp án sai hoặc có đáp án thứ hai; citation trỏ sai mục; `source.text` khái quát vượt nguồn; và công thức “Dân biết, dân bàn, dân làm, dân kiểm tra” từng bị ghép thêm hai vế không có trong snapshot.

Remediation giữ nguyên 280 ID và ma trận môn học, loại padding, viết lại distractor thành near-miss cùng phạm trù, chuyển đủ 56 câu Vận dụng thành tình huống, sửa khóa/citation/explanation và bảo toàn phân phối đáp án A/B/C/D `70/70/70/70`.

## Review chéo độc lập

- Reviewer A biên tập Chương 1–2; Reviewer C đọc độc lập 80/80 câu, thử bảo vệ từng distractor và kiểm 16/16 câu Vận dụng. Các finding `C01-Q013`, `C02-Q015`, `C02-Q030` được sửa và re-review đến khi đóng.
- Reviewer B biên tập Chương 3–4; Reviewer C đọc độc lập 85/85 câu và 17/17 câu Vận dụng. Mười ba miskey, `C03-Q044` và các citation liên quan được sửa; reviewer xác nhận lại đúng diff cuối.
- Reviewer C biên tập Chương 5–7; Reviewer B đọc độc lập 115/115 câu và 23/23 câu Vận dụng. Các finding tại Chương 5–7, gồm locator/evidence `C06-Q037`, `Q041–Q045`, được sửa và re-review trên hash cuối.

Mỗi chương vì vậy có một reviewer độc lập không phải người biên tập chương đó. Không còn finding Critical, High hoặc Medium mở.

## Kết quả kiểm định

- Validator repository: `280 câu · 0 error · 0 warning`.
- Validator nghiêm ngặt của skill: `280 câu · 0 error · 0 warning`.
- Độ khó: `112 Nhận biết / 112 Thông hiểu / 56 Vận dụng`.
- Vị trí đáp án: `A/B/C/D = 70/70/70/70`.
- Không còn padding bị cấm, HTML/unsafe token, phương án trùng, stem trùng đáng kể hay cửa sổ độ dài làm lộ đáp án.

Kết luận: **APPROVED / READY** cho đúng canonical bank hash và bảy chapter hash trong `review-signoff.json`. Mọi sửa đổi câu hỏi sau thời điểm này làm sign-off mất hiệu lực và phải review, ký lại.
