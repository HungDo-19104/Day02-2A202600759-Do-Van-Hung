# 01 — Individual Problem Scan

## 1. Scan rộng: 5+ vấn đề quan sát được

Mục tiêu của phần này là bắt đầu từ vấn đề thật trong học tập, tìm việc và an toàn giao thông. Tôi không bắt đầu bằng việc chọn sẵn một giải pháp AI, mà tập trung vào các vấn đề có actor rõ ràng, workflow hiện tại và dấu hiệu đau thật.

| # | Lăng kính | Vấn đề quan sát được | Ai đang đau? | Dấu hiệu / evidence ban đầu | Mức AI phù hợp ban đầu |
|---|---|---|---|---|---|
| 1 | AI có thể tốt hơn | Người học AI phải đọc paper tiếng Anh nên thường mất nhiều thời gian dịch và hiểu nội dung | Sinh viên AI, người nghiên cứu AI | Mỗi paper có thể mất 1-2 tiếng để đọc, nhiều người phải copy từng đoạn sang ChatGPT hoặc Google Translate | Workflow |
| 2 | Tốn thời gian | Sinh viên mới ra trường phải chỉnh sửa CV cho từng JD tuyển dụng | Sinh viên năm cuối, fresher | Mỗi lần ứng tuyển mất 30-60 phút chỉnh CV, nhiều người không biết CV có phù hợp JD hay không | Workflow |
| 3 | Pain từ người khác | Hệ thống cảnh báo ngủ gật hiện tại thường chỉ phát hiện khi tài xế đã bắt đầu ngủ gật thay vì cảnh báo sớm khi xuất hiện dấu hiệu buồn ngủ | Tài xế xe tải, taxi, xe khách đường dài | Tai nạn do buồn ngủ vẫn xảy ra dù có camera giám sát, cảnh báo thường xuất hiện quá muộn để người lái phản ứng | Workflow / AI Model |

---

## 2. Top 3 vấn đề được chọn

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Phát hiện tiền ngủ gật cho tài xế | Impact lớn, có thể cứu người, actor và pain rất rõ | Cần dữ liệu và cách đo trạng thái "sắp ngủ gật" |
| 2 | Tối ưu CV theo JD tuyển dụng | Pain thực tế với sinh viên mới ra trường, dễ đo hiệu quả | Khó chứng minh tỷ lệ đậu phỏng vấn tăng bao nhiêu |
| 3 | Dịch paper tiếng Anh giữ nguyên cấu trúc | Gần với trải nghiệm học AI, workflow rõ | Đã có nhiều công cụ tương tự trên thị trường |

---

## 3. Problem Card #1 — Phát hiện tiền ngủ gật cho tài xế

### Problem 1 câu

Tài xế thường chỉ được cảnh báo khi đã bắt đầu ngủ gật, trong khi các dấu hiệu buồn ngủ xuất hiện từ trước đó và có thể được phát hiện sớm.

### Actor

Tài xế xe tải, taxi, xe khách đường dài.

### Current workflow

```text
1. Tài xế lái xe trong thời gian dài
2. Xuất hiện dấu hiệu mệt mỏi
3. Chớp mắt nhiều, ngáp, mất tập trung
4. Hệ thống không phát hiện được
5. Bắt đầu ngủ gật
6. Cảnh báo hoặc tai nạn xảy ra
```

### Bottleneck

Các hệ thống hiện tại thường phản ứng khi tài xế đã rơi vào trạng thái ngủ gật thay vì dự đoán sớm.

### Success metric

- Cảnh báo trước khi ngủ gật ít nhất 30 giây
- Giảm tỷ lệ cảnh báo muộn
- Độ chính xác phát hiện > 85%

### Non-AI alternative

Nghỉ giải lao định kỳ, cảm biến thời gian lái xe.

### AI hypothesis

Sử dụng camera và AI để theo dõi mắt, khuôn mặt, tần suất chớp mắt, ngáp và tư thế đầu nhằm dự đoán nguy cơ ngủ gật.

### Quick gut

**Workflow + AI Model**

---

## 4. Problem Card #2 — Tối ưu CV theo JD tuyển dụng

### Problem 1 câu

Sinh viên mới ra trường thường không biết cách điều chỉnh CV theo từng JD nên mất nhiều thời gian và giảm khả năng được gọi phỏng vấn.

### Actor

Sinh viên năm cuối, fresher.

### Current workflow

```text
1. Tìm JD tuyển dụng
2. Đọc yêu cầu công việc
3. So sánh với CV hiện tại
4. Chỉnh sửa CV
5. Viết cover letter
6. Nộp hồ sơ
```

### Bottleneck

Người dùng không biết kỹ năng nào cần nhấn mạnh hoặc CV đang thiếu điều gì so với JD.

### Success metric

- Giảm thời gian chỉnh CV xuống dưới 10 phút
- Tăng số lượng hồ sơ ứng tuyển mỗi tuần
- Tăng tỷ lệ phản hồi từ HR

### Non-AI alternative

Sử dụng mẫu CV chuẩn và tự chỉnh sửa thủ công.

### AI hypothesis

AI phân tích JD, chấm mức độ phù hợp của CV và đề xuất chỉnh sửa.

### Quick gut

**Workflow**

---

## 5. Problem Card #3 — Dịch paper tiếng Anh giữ nguyên cấu trúc

### Problem 1 câu

Người học AI gặp khó khăn khi đọc paper tiếng Anh vì phải vừa dịch nội dung vừa cố giữ cấu trúc học thuật của tài liệu.

### Actor

Sinh viên AI, người nghiên cứu AI.

### Current workflow

```text
1. Tìm paper
2. Đọc abstract
3. Copy từng đoạn sang công cụ dịch
4. Ghép kết quả dịch
5. Đọc lại để hiểu nội dung
```

### Bottleneck

Việc dịch thủ công làm mất thời gian và dễ phá vỡ bố cục, bảng biểu, công thức của paper.

### Success metric

- Giảm 50% thời gian đọc paper
- Giữ nguyên heading, hình ảnh và công thức
- Tăng khả năng hiểu nội dung của người đọc

### Non-AI alternative

Dùng Google Translate hoặc đọc bản gốc tiếng Anh.

### AI hypothesis

AI phân tích PDF, giữ nguyên layout và dịch nội dung sang tiếng Việt theo ngữ cảnh học thuật.

### Quick gut

**Workflow**
