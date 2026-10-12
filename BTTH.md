# Bài làm: Từ Backlog cũ đến Backlog chuẩn: Module "Đánh giá sản phẩm" (GreenCart)

## Phần A: Chẩn đoán hiện trạng

### 1. Đánh giá S1
- Trạng thái: Đúng.
- Lý do: S1 viết đúng cấu trúc 3 thành phần (As a... I want... So that...) và đạt tiêu chuẩn INVEST: mang lại giá trị độc lập cho người dùng, phạm vi vừa vặn để làm trong một Sprint, có thể kiểm thử và nghiệm thu rõ ràng.

### 2. Đánh giá S2
- Trạng thái: Sai.
- Lỗi cấp độ: S2 bị nhầm cấp độ phân rã. Đây thực chất là một Feature hoặc Epic nhỏ chứ không thể là một User Story đơn lẻ.
- Vi phạm các tiêu chí INVEST:
  - Vi phạm Small (S): Gộp quá nhiều nghiệp vụ vào cùng một mục (chấm sao, viết bình luận, đính kèm ảnh, gửi bài, admin kiểm duyệt, hiển thị lên trang).
  - Vi phạm Independent (I): Trộn lẫn thao tác của người mua hàng với khâu duyệt bài của quản trị viên hệ thống.
  - Vi phạm Estimable (E): Phạm vi quá rộng và chung chung khiến Dev không thể ước lượng chính xác nỗ lực và thời gian thực hiện.
  - Sai cú pháp: Viết theo kiểu đặt tên tính năng hệ thống ("Hệ thống đánh giá sản phẩm"), không dùng cấu trúc User Story (As a... I want... So that...).

### 3. Vì sao S2 không thể đưa thẳng vào Sprint Backlog?
S2 có phạm vi quá lớn, không thể hoàn thành trong một Sprint và chưa đạt chuẩn Definition of Ready (DoR). Nội dung này chưa được làm mịn (refine) nên Dev không thể bóc tách thành các công việc cụ thể (Tasks) để thực hiện trong Sprint.

---

## Phần B: Hoàn thiện Backlog

### 1. Đặt tên Feature F2
- Tên Feature: `F2: Xem và tham khảo đánh giá sản phẩm` (Viewing & Browsing Product Reviews)

### 2. Bổ sung User Story S3 (thuộc Feature F1)
- User Story S3:  
  As a khách hàng đã mua sản phẩm,  
  I want viết nhận xét chi tiết và tải lên tối đa 3 ảnh chụp thực tế,  
  so that tôi chia sẻ trải nghiệm thực tế cho người mua sau tham khảo.

### 3. Thiết kế User Story thuộc Feature F2
- US F2.1:  
  As a người mua hàng,  
  I want xem điểm đánh giá trung bình và tổng số lượt đánh giá của sản phẩm,  
  so that tôi nắm được mức độ hài lòng chung của người mua trước khi quyết định mua.
- US F2.2:  
  As a người mua hàng,  
  I want xem danh sách các bình luận đánh giá kèm hình ảnh thực tế từ người mua trước,  
  so that tôi nắm rõ ưu nhược điểm cụ thể của sản phẩm.

### 4. Tách S2 thành 3 User Story độc lập đạt chuẩn INVEST

1. US 2a (Gửi đánh giá kèm nhận xét):  
   As a khách hàng đã mua sản phẩm,  
   I want nhập nội dung nhận xét và gửi đánh giá sản phẩm,  
   so that tôi đóng góp ý kiến về sản phẩm cho cửa hàng và người mua khác tham khảo.

2. US 2b (Kiểm duyệt nội dung đánh giá):  
   As an Admin (Quản trị viên),  
   I want hệ thống tự động lọc các từ ngữ phản cảm và cho phép tôi duyệt hoặc từ chối các đánh giá,  
   so that trang web không bị hiển thị các nội dung rác hoặc phản cảm.

3. US 2c (Hiển thị đánh giá công khai):  
   As a người xem sản phẩm,  
   I want xem các bình luận đánh giá đã qua phê duyệt trên trang chi tiết sản phẩm,  
   so that tôi có thêm thông tin thực tế trước khi bấm đặt mua.
