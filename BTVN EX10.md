# **BÀI LÀM: PHÂN TÍCH VÀ SO SÁNH HAI CHIẾN LƯỢC VIẾT PROMPT BẰNG MARKDOWN**

## **Phần 1: Phân tích và đề xuất**

### **1\. Phân tích yêu cầu đầu vào và đầu ra (I/O)**

\- Input (đầu vào):

* Người hỏi là sinh viên năm nhất PTIT, chưa có nền tảng lập trình.  
* Khái niệm cần tìm hiểu là Markdown Parser.  
* Người dùng muốn được giải thích đơn giản, dễ hiểu và phù hợp với trình độ của mình.

\- Output (đầu ra):

* AI giải thích đúng khái niệm Markdown Parser bằng ngôn ngữ đời thường.  
* Có ví dụ cụ thể về một câu Markdown và kết quả hiển thị.  
* Nội dung ngắn gọn, không sử dụng quá nhiều thuật ngữ chuyên ngành.

### **2\. Ưu điểm và nhược điểm của hai chiến lược**

Chiến lược A: Văn xuôi thuần túy

\- Ưu điểm:

* Prompt ngắn gọn, dễ viết và dễ sử dụng.  
* Tiết kiệm token, phù hợp với những câu hỏi đơn giản.  
* Người mới có thể áp dụng ngay mà không cần học cú pháp Markdown.

\- Nhược điểm:

* Yêu cầu chưa cụ thể về độ dài và cách trình bày.  
* AI có thể trả lời quá dài hoặc thiếu ví dụ minh họa.  
* Khó tái sử dụng cho những nhiệm vụ phức tạp hoặc cần đầu ra nhất quán.

Chiến lược B: Cấu trúc Markdown 3 phần

\- Ưu điểm:

* Phân chia rõ bối cảnh, khái niệm cần giải thích và yêu cầu.  
* Giúp AI hiểu rõ trình độ người học và cách trình bày mong muốn.  
* Dễ chỉnh sửa, tái sử dụng cho nhiều khái niệm khác nhau.  
* Hạn chế câu trả lời quá dài hoặc chứa kiến thức vượt trình độ.

\- Nhược điểm:

* Prompt dài hơn, tiêu thụ nhiều token hơn.  
* Người mới cần biết cách sử dụng tiêu đề Markdown như `##`.  
* Nếu đặt yêu cầu sai mục hoặc viết các chỉ dẫn mâu thuẫn, AI có thể hiểu không chính xác.

## **Phần 2: So sánh và lựa chọn**

### **3\. Bảng so sánh theo 4 tiêu chí**

| Tiêu chí | Chiến lược A: Văn xuôi | Chiến lược B: Markdown 3 phần |
| ----- | ----- | ----- |
| Độ chính xác | Khá, vì yêu cầu còn chung chung | Cao hơn, vì yêu cầu rõ ràng |
| Tiêu thụ Token | Ít hơn | Nhiều hơn |
| Khả năng tái sử dụng | Thấp đến trung bình | Cao, chỉ cần đổi khái niệm và điều chỉnh yêu cầu |
| Dễ học cho người mới | Rất dễ | Dễ sau khi biết cú pháp cơ bản |

### **4\. Chốt lựa chọn**

\- Nên dùng chiến lược A khi cần hỏi nhanh một câu hỏi đơn giản, tìm hiểu sơ bộ một khái niệm hoặc trao đổi tự nhiên với AI. Cách này tiết kiệm token và không yêu cầu người dùng phải biết Markdown.

\- Nên dùng chiến lược B khi ôn thi, làm bài tập hoặc cần AI giải thích theo một khuôn mẫu cụ thể. Dù tốn nhiều token hơn, chiến lược này giúp câu trả lời có cấu trúc, đúng trình độ và dễ kiểm soát.

Lựa chọn phù hợp nhất cho sinh viên năm nhất PTIT: Chiến lược B, vì người học cần kiến thức dễ hiểu, có ví dụ và có thể áp dụng lại cho nhiều bài học IT-101.

## **Phần 3: Thiết kế và triển khai**

### **5\. Thiết kế Prompt mẫu để hỏi về khái niệm Token**

Có thể sử dụng Prompt theo cấu trúc Markdown 3 phần sau:

## **Bối cảnh**

Tôi là sinh viên năm nhất PTIT, chưa có nền tảng lập trình và đang học môn Nhập môn Công nghệ thông tin.

## **Khái niệm cần giải thích**

Token trong AI.

## **Yêu cầu**

* Giải thích bằng ngôn ngữ đời thường, dễ hiểu.  
* Sử dụng một ví dụ quen thuộc trong cuộc sống để minh họa.  
* Trình bày trong khoảng 100-150 từ.  
* Cho một ví dụ cụ thể để tôi hiểu cách AI chia văn bản thành các token.

## **Không cần**

* Thuật ngữ kỹ thuật phức tạp.  
* Công thức toán học.  
* Ví dụ lập trình dài.

### **6\. Trả lời hai bẫy dữ liệu**

Bẫy 1: Nếu đặt yêu cầu độ dài vào sai phần, AI có hiểu đúng không?

AI vẫn có khả năng hiểu yêu cầu vì nó đọc toàn bộ Prompt, không chỉ đọc từng phần riêng biệt. Tuy nhiên, việc đặt yêu cầu sai mục có thể làm giảm tính rõ ràng, khiến AI khó phân biệt đâu là thông tin bối cảnh, đâu là chỉ dẫn cần thực hiện.

Ví dụ, đặt “Giải thích trong 100-150 từ” vào phần `## Bối cảnh` thay vì `## Yêu cầu` có thể khiến cấu trúc Prompt thiếu logic. Vì vậy, cần đặt mỗi thông tin đúng mục để tăng tính nhất quán và giảm khả năng hiểu nhầm.

Bẫy 2: Khi nào nên ưu tiên chiến lược A thay vì B?

Nên ưu tiên chiến lược A khi:

* Câu hỏi đơn giản, không cần câu trả lời theo khuôn mẫu.  
* Chỉ cần giải thích nhanh hoặc hỏi thêm một ý nhỏ trong cuộc hội thoại.  
* Muốn tiết kiệm token và thời gian nhập Prompt.  
* Đang trao đổi tự nhiên với AI và có thể bổ sung yêu cầu qua các lượt hỏi tiếp theo.

Ngược lại, chiến lược B phù hợp hơn khi cần câu trả lời có độ dài, định dạng và ví dụ cụ thể.

Lưu ý rằng Prompt dài hơn không tự động làm AI trả lời chính xác hơn. Hiệu quả phụ thuộc vào mức độ rõ ràng, phù hợp và nhất quán của các yêu cầu.

## **Kết luận**

Cả hai chiến lược đều có ưu điểm riêng. Chiến lược A phù hợp với câu hỏi nhanh, đơn giản; chiến lược B phù hợp với nhiệm vụ học tập có yêu cầu cụ thể. Đối với sinh viên năm nhất đang ôn thi IT-101, nên ưu tiên chiến lược B để có câu trả lời rõ ràng, dễ hiểu và có thể tái sử dụng, đồng thời dùng chiến lược A khi cần trao đổi nhanh hoặc làm rõ kiến thức.

