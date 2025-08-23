<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "9b4c2650691b24b20e0c912d01a466a2",
  "translation_date": "2025-08-21T13:27:36+00:00",
  "source_file": "README.md",
  "language_code": "vi"
}
-->
# Các Tác Nhân AI cho Người Mới Bắt Đầu - Một Khóa Học

![Generative AI For Beginners](../../translated_images/repo-thumbnail.083b24afed61b6dd27a7fc53798bebe9edf688a41031163a1fca9f61c64d63ec.vi.png)

## 11 bài học dạy mọi thứ bạn cần biết để bắt đầu xây dựng các Tác Nhân AI

[![GitHub license](https://img.shields.io/github/license/microsoft/ai-agents-for-beginners.svg)](https://github.com/microsoft/ai-agents-for-beginners/blob/master/LICENSE?WT.mc_id=academic-105485-koreyst)  
[![GitHub contributors](https://img.shields.io/github/contributors/microsoft/ai-agents-for-beginners.svg)](https://GitHub.com/microsoft/ai-agents-for-beginners/graphs/contributors/?WT.mc_id=academic-105485-koreyst)  
[![GitHub issues](https://img.shields.io/github/issues/microsoft/ai-agents-for-beginners.svg)](https://GitHub.com/microsoft/ai-agents-for-beginners/issues/?WT.mc_id=academic-105485-koreyst)  
[![GitHub pull-requests](https://img.shields.io/github/issues-pr/microsoft/ai-agents-for-beginners.svg)](https://GitHub.com/microsoft/ai-agents-for-beginners/pulls/?WT.mc_id=academic-105485-koreyst)  
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com?WT.mc_id=academic-105485-koreyst)

### 🌐 Hỗ Trợ Đa Ngôn Ngữ

#### Được hỗ trợ qua GitHub Action (Tự động & Luôn cập nhật)

[French](../fr/README.md) | [Spanish](../es/README.md) | [German](../de/README.md) | [Russian](../ru/README.md) | [Arabic](../ar/README.md) | [Persian (Farsi)](../fa/README.md) | [Urdu](../ur/README.md) | [Chinese (Simplified)](../zh/README.md) | [Chinese (Traditional, Macau)](../mo/README.md) | [Chinese (Traditional, Hong Kong)](../hk/README.md) | [Chinese (Traditional, Taiwan)](../tw/README.md) | [Japanese](../ja/README.md) | [Korean](../ko/README.md) | [Hindi](../hi/README.md) | [Bengali](../bn/README.md) | [Marathi](../mr/README.md) | [Nepali](../ne/README.md) | [Punjabi (Gurmukhi)](../pa/README.md) | [Portuguese (Portugal)](../pt/README.md) | [Portuguese (Brazil)](../br/README.md) | [Italian](../it/README.md) | [Polish](../pl/README.md) | [Turkish](../tr/README.md) | [Greek](../el/README.md) | [Thai](../th/README.md) | [Swedish](../sv/README.md) | [Danish](../da/README.md) | [Norwegian](../no/README.md) | [Finnish](../fi/README.md) | [Dutch](../nl/README.md) | [Hebrew](../he/README.md) | [Vietnamese](./README.md) | [Indonesian](../id/README.md) | [Malay](../ms/README.md) | [Tagalog (Filipino)](../tl/README.md) | [Swahili](../sw/README.md) | [Hungarian](../hu/README.md) | [Czech](../cs/README.md) | [Slovak](../sk/README.md) | [Romanian](../ro/README.md) | [Bulgarian](../bg/README.md) | [Serbian (Cyrillic)](../sr/README.md) | [Croatian](../hr/README.md) | [Slovenian](../sl/README.md) | [Ukrainian](../uk/README.md) | [Burmese (Myanmar)](../my/README.md)

**Nếu bạn muốn có thêm ngôn ngữ được hỗ trợ, danh sách các ngôn ngữ có sẵn [ở đây](https://github.com/Azure/co-op-translator/blob/main/getting_started/supported-languages.md)**

[![GitHub watchers](https://img.shields.io/github/watchers/microsoft/ai-agents-for-beginners.svg?style=social&label=Watch)](https://GitHub.com/microsoft/ai-agents-for-beginners/watchers/?WT.mc_id=academic-105485-koreyst)  
[![GitHub forks](https://img.shields.io/github/forks/microsoft/ai-agents-for-beginners.svg?style=social&label=Fork)](https://GitHub.com/microsoft/ai-agents-for-beginners/network/?WT.mc_id=academic-105485-koreyst)  
[![GitHub stars](https://img.shields.io/github/stars/microsoft/ai-agents-for-beginners.svg?style=social&label=Star)](https://GitHub.com/microsoft/ai-agents-for-beginners/stargazers/?WT.mc_id=academic-105485-koreyst)

[![Azure AI Discord](https://dcbadge.limes.pink/api/server/kzRShWzttr)](https://discord.gg/kzRShWzttr)

## 🌱 Bắt Đầu

Khóa học này bao gồm 11 bài học về các nguyên tắc cơ bản để xây dựng Tác Nhân AI. Mỗi bài học tập trung vào một chủ đề riêng, vì vậy bạn có thể bắt đầu từ bất kỳ đâu!

Khóa học này hỗ trợ đa ngôn ngữ. Hãy xem [các ngôn ngữ có sẵn tại đây](../..).

Nếu đây là lần đầu tiên bạn làm việc với các mô hình Generative AI, hãy tham khảo khóa học [Generative AI For Beginners](https://aka.ms/genai-beginners), bao gồm 21 bài học về xây dựng với GenAI.

Đừng quên [gắn sao (🌟) repo này](https://docs.github.com/en/get-started/exploring-projects-on-github/saving-repositories-with-stars?WT.mc_id=academic-105485-koreyst) và [fork repo này](https://github.com/microsoft/ai-agents-for-beginners/fork) để chạy mã.

### Những Gì Bạn Cần

Mỗi bài học trong khóa học này bao gồm các ví dụ mã, được tìm thấy trong thư mục code_samples. Bạn có thể [fork repo này](https://github.com/microsoft/ai-agents-for-beginners/fork) để tạo bản sao của riêng bạn.

Các ví dụ mã trong các bài tập này sử dụng Azure AI Foundry và GitHub Model Catalogs để tương tác với các Mô Hình Ngôn Ngữ:

- [Github Models](https://aka.ms/ai-agents-beginners/github-models) - Miễn phí / Giới hạn  
- [Azure AI Foundry](https://aka.ms/ai-agents-beginners/ai-foundry) - Yêu cầu tài khoản Azure  

Khóa học này cũng sử dụng các framework và dịch vụ Tác Nhân AI sau từ Microsoft:

- [Azure AI Agent Service](https://aka.ms/ai-agents-beginners/ai-agent-service)  
- [Semantic Kernel](https://aka.ms/ai-agents-beginners/semantic-kernel)  
- [AutoGen](https://aka.ms/ai-agents/autogen)  

Để biết thêm thông tin về cách chạy mã cho khóa học này, hãy xem [Cài Đặt Khóa Học](./00-course-setup/README.md).

## 🙏 Muốn giúp đỡ?

Bạn có đề xuất hoặc phát hiện lỗi chính tả hoặc mã? [Tạo một issue](https://github.com/microsoft/ai-agents-for-beginners/issues?WT.mc_id=academic-105485-koreyst) hoặc [Tạo một pull request](https://github.com/microsoft/ai-agents-for-beginners/pulls?WT.mc_id=academic-105485-koreyst).

Nếu bạn gặp khó khăn hoặc có bất kỳ câu hỏi nào về việc xây dựng Tác Nhân AI, hãy tham gia [Cộng Đồng Azure AI Foundry trên Discord](https://discord.gg/kzRShWzttr).

Nếu bạn có phản hồi sản phẩm hoặc gặp lỗi trong quá trình xây dựng, hãy truy cập [Diễn Đàn Nhà Phát Triển Azure AI Foundry](https://aka.ms/azureaifoundry/forum).

## 📂 Mỗi bài học bao gồm

- Một bài học viết trong README và một video ngắn  
- Các ví dụ mã Python hỗ trợ Azure AI Foundry và Github Models (Miễn phí)  
- Liên kết đến các tài nguyên bổ sung để tiếp tục học tập  

## 🗃️ Các Bài Học

| **Bài Học**                              | **Văn Bản & Mã**                                  | **Video**                                                  | **Học Thêm**                                                                         |
|------------------------------------------|---------------------------------------------------|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| Giới thiệu về Tác Nhân AI và Các Trường Hợp Sử Dụng | [Link](./01-intro-to-ai-agents/README.md)         | [Video](https://youtu.be/3zgm60bXmQk?si=z8QygFvYQv-9WtO1)  | [Link](https://aka.ms/ai-agents-beginners/collection?WT.mc_id=academic-105485-koreyst) |
| Khám phá các Framework Tác Nhân AI       | [Link](./02-explore-agentic-frameworks/README.md) | [Video](https://youtu.be/ODwF-EZo_O8?si=Vawth4hzVaHv-u0H)  | [Link](https://aka.ms/ai-agents-beginners/collection?WT.mc_id=academic-105485-koreyst) |
| Hiểu về Mẫu Thiết Kế Tác Nhân AI         | [Link](./03-agentic-design-patterns/README.md)    | [Video](https://youtu.be/m9lM8qqoOEA?si=BIzHwzstTPL8o9GF)  | [Link](https://aka.ms/ai-agents-beginners/collection?WT.mc_id=academic-105485-koreyst) |
| Mẫu Thiết Kế Sử Dụng Công Cụ             | [Link](./04-tool-use/README.md)                   | [Video](https://youtu.be/vieRiPRx-gI?si=2z6O2Xu2cu_Jz46N)  | [Link](https://aka.ms/ai-agents-beginners/collection?WT.mc_id=academic-105485-koreyst) |
| Tác Nhân RAG                             | [Link](./05-agentic-rag/README.md)                | [Video](https://youtu.be/WcjAARvdL7I?si=gKPWsQpKiIlDH9A3)  | [Link](https://aka.ms/ai-agents-beginners/collection?WT.mc_id=academic-105485-koreyst) |
| Xây dựng Tác Nhân AI Đáng Tin Cậy        | [Link](./06-building-trustworthy-agents/README.md)| [Video](https://youtu.be/iZKkMEGBCUQ?si=jZjpiMnGFOE9L8OK)  | [Link](https://aka.ms/ai-agents-beginners/collection?WT.mc_id=academic-105485-koreyst) |
| Mẫu Thiết Kế Lập Kế Hoạch                | [Link](./07-planning-design/README.md)            | [Video](https://youtu.be/kPfJ2BrBCMY?si=6SC_iv_E5-mzucnC)  | [Link](https://aka.ms/ai-agents-beginners/collection?WT.mc_id=academic-105485-koreyst) |
| Mẫu Thiết Kế Đa Tác Nhân                 | [Link](./08-multi-agent/README.md)                | [Video](https://youtu.be/V6HpE9hZEx0?si=rMgDhEu7wXo2uo6g)  | [Link](https://aka.ms/ai-agents-beginners/collection?WT.mc_id=academic-105485-koreyst) |
| Mẫu Thiết Kế Siêu Nhận Thức              | [Link](./09-metacognition/README.md)              | [Video](https://youtu.be/His9R6gw6Ec?si=8gck6vvdSNCt6OcF)  | [Link](https://aka.ms/ai-agents-beginners/collection?WT.mc_id=academic-105485-koreyst) |
| Tác Nhân AI Trong Sản Xuất               | [Link](./10-ai-agents-production/README.md)       | [Video](https://youtu.be/l4TP6IyJxmQ?si=31dnhexRo6yLRJDl)  | [Link](https://aka.ms/ai-agents-beginners/collection?WT.mc_id=academic-105485-koreyst) |
| Tác Nhân AI với MCP                      | [Link](./11-mcp/README.md)                        |                                                            | [Link](https://aka.ms/mcp-for-beginners)                                             |

## 🎒 Các Khóa Học Khác

Nhóm của chúng tôi còn sản xuất các khóa học khác! Hãy xem:
- [**MỚI** Giao thức Ngữ cảnh Mô hình (MCP) Dành cho Người Mới Bắt Đầu](https://github.com/microsoft/mcp-for-beginners?WT.mc_id=academic-105485-koreyst)  
- [AI Tạo Sinh Dành cho Người Mới Bắt Đầu sử dụng .NET](https://github.com/microsoft/Generative-AI-for-beginners-dotnet?WT.mc_id=academic-105485-koreyst)  
- [AI Tạo Sinh Dành cho Người Mới Bắt Đầu](https://github.com/microsoft/generative-ai-for-beginners?WT.mc_id=academic-105485-koreyst)  
- [AI Tạo Sinh Dành cho Người Mới Bắt Đầu sử dụng Java](https://github.com/microsoft/generative-ai-for-beginners-java?WT.mc_id=academic-105485-koreyst)  
- [Học Máy Dành cho Người Mới Bắt Đầu](https://aka.ms/ml-beginners?WT.mc_id=academic-105485-koreyst)  
- [Khoa Học Dữ Liệu Dành cho Người Mới Bắt Đầu](https://aka.ms/datascience-beginners?WT.mc_id=academic-105485-koreyst)  
- [Trí Tuệ Nhân Tạo Dành cho Người Mới Bắt Đầu](https://aka.ms/ai-beginners?WT.mc_id=academic-105485-koreyst)  
- [An Ninh Mạng Dành cho Người Mới Bắt Đầu](https://github.com/microsoft/Security-101??WT.mc_id=academic-96948-sayoung)  
- [Phát Triển Web Dành cho Người Mới Bắt Đầu](https://aka.ms/webdev-beginners?WT.mc_id=academic-105485-koreyst)  
- [IoT Dành cho Người Mới Bắt Đầu](https://aka.ms/iot-beginners?WT.mc_id=academic-105485-koreyst)  
- [Phát Triển XR Dành cho Người Mới Bắt Đầu](https://github.com/microsoft/xr-development-for-beginners?WT.mc_id=academic-105485-koreyst)  
- [Thành Thạo GitHub Copilot cho Lập Trình Cặp AI](https://aka.ms/GitHubCopilotAI?WT.mc_id=academic-105485-koreyst)  
- [Thành Thạo GitHub Copilot cho Nhà Phát Triển C#/.NET](https://github.com/microsoft/mastering-github-copilot-for-dotnet-csharp-developers?WT.mc_id=academic-105485-koreyst)  
- [Chọn Cuộc Phiêu Lưu Copilot của Riêng Bạn](https://github.com/microsoft/CopilotAdventures?WT.mc_id=academic-105485-koreyst)  

## 🌟 Cảm Ơn Cộng Đồng  

Cảm ơn [Shivam Goyal](https://www.linkedin.com/in/shivam2003/) đã đóng góp các mẫu mã quan trọng minh họa Agentic RAG.  

## Đóng Góp  

Dự án này hoan nghênh các đóng góp và gợi ý. Hầu hết các đóng góp yêu cầu bạn đồng ý với Thỏa Thuận Giấy Phép Người Đóng Góp (CLA) tuyên bố rằng bạn có quyền và thực sự cấp cho chúng tôi quyền sử dụng đóng góp của bạn. Để biết chi tiết, hãy truy cập  
<https://cla.opensource.microsoft.com>.  

Khi bạn gửi một yêu cầu pull, bot CLA sẽ tự động xác định xem bạn có cần cung cấp CLA hay không và đánh dấu PR một cách phù hợp (ví dụ: kiểm tra trạng thái, bình luận). Chỉ cần làm theo hướng dẫn được cung cấp bởi bot. Bạn chỉ cần làm điều này một lần trên tất cả các kho lưu trữ sử dụng CLA của chúng tôi.  

Dự án này đã áp dụng [Bộ Quy Tắc Ứng Xử Mã Nguồn Mở của Microsoft](https://opensource.microsoft.com/codeofconduct/).  
Để biết thêm thông tin, hãy xem [Câu Hỏi Thường Gặp về Quy Tắc Ứng Xử](https://opensource.microsoft.com/codeofconduct/faq/) hoặc liên hệ [opencode@microsoft.com](mailto:opencode@microsoft.com) với bất kỳ câu hỏi hoặc ý kiến bổ sung nào.  

## Thương Hiệu  

Dự án này có thể chứa các thương hiệu hoặc logo cho các dự án, sản phẩm hoặc dịch vụ. Việc sử dụng hợp pháp các thương hiệu hoặc logo của Microsoft phải tuân theo và tuân thủ  
[Hướng Dẫn Thương Hiệu & Nhãn Hiệu của Microsoft](https://www.microsoft.com/legal/intellectualproperty/trademarks/usage/general).  
Việc sử dụng các thương hiệu hoặc logo của Microsoft trong các phiên bản sửa đổi của dự án này không được gây nhầm lẫn hoặc ngụ ý tài trợ từ Microsoft.  
Bất kỳ việc sử dụng thương hiệu hoặc logo của bên thứ ba nào phải tuân theo chính sách của bên thứ ba đó.  

**Tuyên bố miễn trừ trách nhiệm**:  
Tài liệu này đã được dịch bằng dịch vụ dịch thuật AI [Co-op Translator](https://github.com/Azure/co-op-translator). Mặc dù chúng tôi cố gắng đảm bảo độ chính xác, xin lưu ý rằng các bản dịch tự động có thể chứa lỗi hoặc không chính xác. Tài liệu gốc bằng ngôn ngữ bản địa nên được coi là nguồn tham khảo chính thức. Đối với các thông tin quan trọng, chúng tôi khuyến nghị sử dụng dịch vụ dịch thuật chuyên nghiệp từ con người. Chúng tôi không chịu trách nhiệm cho bất kỳ sự hiểu lầm hoặc diễn giải sai nào phát sinh từ việc sử dụng bản dịch này.